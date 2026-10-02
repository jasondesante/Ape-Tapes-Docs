# Mixes End To End

Alternate mixes live in two layers. The track's metadata declares what mixes exist and what conditions unlock them. The playlist entry pins which one plays. This page walks one complete entry through both layers — the raw playlist object, the metadata behind it, and what a player resolves out of the pair.

Every condition type used here is in the [Grouped Traits](../../../create/the-metadata-maker/metadata-standards/token-metadata/grouped-traits.md#mixes) reference.

### 1. The Raw Playlist Entry

One track object from the playlist's `tracks` array. `selected_mix` pins "Extended VIP". Note that `audio_url` is just the track's primary audio at this point — nothing about the mix has been applied yet:

```json
{
  "title": "I'm With The DJ",
  "chain_name": "ethereum",
  "platform": "contract-wizard",
  "token_address": "0xF956b9B324ec32BFeC53cF4eEf33578371692658",
  "token_id": "7",
  "id": "ethereum/0xF956b9B324ec32BFeC53cF4eEf33578371692658/7",
  "uuid": "00537132-5b69-46ae-9789-e0dc7213f341",
  "playlist_index": 1,
  "selected_mix": "Extended VIP",
  "audio_url": "https://arweave.net/abc123",
  "artwork_url": "https://arweave.net/def456"
}
```

The pin is the only mix-related field on the entry. Everything else the player needs is inside the metadata.

### 2. The Metadata Behind It

Here is the entry's stringified `metadata` field, shown parsed. The `mixes` array declares three mixes: "Extended VIP" twice — a lossy mp3 master and a lossless wav sharing one name — and "Alt Outro", which points at a metadata file rather than audio:

```json
{
  "name": "I'm With The DJ",
  "artist": "DJ Sanguine",
  "image": "https://arweave.net/def456",
  "animation_url": "https://arweave.net/abc123",
  "mp3_url": "https://arweave.net/abc123",
  "lossless_audio": "https://arweave.net/ghi789",
  "attributes": [
    { "trait_type": "Playlist Index", "value": 1 },
    { "trait_type": "Chain Name", "value": "ethereum" },
    { "trait_type": "Selected Mix", "value": "Extended VIP" }
  ],
  "mixes": [
    {
      "name": "Extended VIP",
      "mime_type": "audio/mpeg",
      "uri": "https://arweave.net/mix001",
      "conditions": [
        { "type": "weight", "value": "3" }
      ]
    },
    {
      "name": "Extended VIP",
      "mime_type": "audio/wav",
      "uri": "https://arweave.net/mix002",
      "conditions": [
        { "type": "weight", "value": "3" }
      ]
    },
    {
      "name": "Alt Outro",
      "mime_type": "application/json",
      "uri": "https://arweave.net/mix003",
      "conditions": [
        { "type": "min_plays", "value": "5" },
        { "type": "favorite", "value": "true" }
      ]
    }
  ]
}
```

Two things worth noticing:

* The `Selected Mix` attribute mirrors the pin, so it shows up on marketplaces next to the other playlist traits. The top-level `selected_mix` field on the entry is canonical; the attribute is the fallback for older playlists.
* The two "Extended VIP" entries carry identical conditions because they are one mix in two qualities, not two mixes. The name is what the pin matches; the `mime_type` tells players which master to prefer.

### 3. The Indirection Mix

"Alt Outro" points at a metadata file, not audio — that's what `mime_type: "application/json"` means. Fetched, it looks like any other track metadata:

```json
{
  "name": "I'm With The DJ (Alt Outro)",
  "image": "https://arweave.net/def456",
  "animation_url": "https://arweave.net/mix004",
  "mp3_url": "https://arweave.net/mix004"
}
```

Players follow it one level and read the audio out of the usual fields — the same [audio field hierarchy](track-metadata.md#audio-field-hierarchy) as any track. The 721J templates ship an example shaped exactly like this, and the indirection is how a mix can carry its own artwork or description without bloating the token metadata.

### 4. What The Player Resolves

Parsing the entry above produces this:

* **"Extended VIP" plays.** The pin matches a name in the `mixes` array exactly and case-sensitively. Two mixes share the name, so the player prefers the lossy master: `audio_url` is repointed at the mp3, and the wav rides along as the lossless option. This happens at parse time, which is why a player can read `audio_url` off the parsed track and never touch the metadata.
* **The pin wins over conditions.** "Extended VIP" carries a `weight`, which shapes random selection — but a pinned mix is a curator's explicit choice, so it plays regardless of what its conditions say.
* **"Alt Outro" stays locked.** It needs five logged plays and a favorited song before it's available; until then a mix picker shows it as locked. Once both conditions are met, playing it follows the indirection one level down to the audio inside.
* **A sloppy pin falls back safely.** `"extended vip"` or `"Extended VIP "` (trailing space) matches nothing and the entry plays the primary audio; `"default"` is treated as absent. Mix names are copied exactly — typos don't error, they just play the default.

The playlist-data-engine implements every step here: `getTrackExtras()` for the mixes, `resolveSelectedMix()` for the pin, `evaluateMixConditions()` for gating, and `selectMix()` / `resolveMixUrl()` for a user's own choice. See [Playlist Data Engine](../../../create/build-your-vision/playlist-data-engine.md).

***

[**Track Objects →**](track-objects.md)\
The playlist entry and its `selected_mix` field

[**Track Metadata →**](track-metadata.md)\
What lives inside the stringified metadata field

[**Grouped Traits →**](../../../create/the-metadata-maker/metadata-standards/token-metadata/grouped-traits.md#mixes)\
Every condition type with its literal `type` value
