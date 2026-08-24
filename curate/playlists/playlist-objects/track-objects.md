# Track Objects

Track objects are the individual entries inside the playlist's tracks array. Each track object represents one piece of music and contains both technical information and the actual audio metadata.

### Track Object Structure

A track object contains multiple types of information:

json

```json
{
  "title": "I'm With The DJ",
  "chain_name": "ethereum", 
  "platform": "sound",
  "token_address": "0xF956b9B324ec32BFeC53cF4eEf33578371692658",
  "token_id": "1",
  "metadata": "{...stringified metadata object...}",
  "id": "ethereum/0xF956b9B324ec32BFeC53cF4eEf33578371692658/1",
  "uuid": "00537132-5b69-46ae-9789-e0dc7213f341",
  "playlist_index": 1,
  "audio_url": "https://arweave.net/abc123...",
  "artwork_url": "https://arweave.net/def456...",
  "audio_ipfs_hash": "Qm...",
  "artwork_ipfs_hash": "Qm..."
}
```

### Field Categories

#### Essential Fields

These fields are present in every track:

* `metadata` - **Most important field** - Stringified JSON containing audio links and track info
* `title` - Track name
* `playlist_index` - Position in playlist
* `uuid` - Unique identifier for duplicate handling

#### Token Fields (When Track is an NFT)

When the track represents a blockchain token:

* `chain_name` - Blockchain network (ethereum, arweave, etc.)
* `token_address` - Contract address
* `token_id` - Token identifier
* `platform` - Minting platform (contract-wizard, sound, catalog, etc.)
* `contract_type` - Contract standard (ERC721, etc.)

#### Technical Fields

Additional identifiers and references:

* `id` - Unique identifier for the track
* `token_uri` - Metadata URL (the metadata field contains this file's contents)
* `name` - Contract name (when applicable)
* `symbol` - Contract symbol (when applicable)

#### Playback Fields

These describe how this entry should be played, as opposed to what the track is:

* `selected_mix` - Name of the mix this playlist entry plays

A track can ship several mixes — radio edit, extended mix, instrumental, and lossless and lossy versions of each. Which one plays is a property of the playlist entry, not of the track, since the same song can sit in two playlists with two different mixes chosen. That is why `selected_mix` lives on the track object in the same layer as `chain_name` and `playlist_index`, rather than inside the stringified metadata:

```json
{
  "title": "I'm With The DJ",
  "chain_name": "ethereum",
  "metadata": "{...stringified metadata object...}",
  "uuid": "00537132-5b69-46ae-9789-e0dc7213f341",
  "playlist_index": 1,
  "selected_mix": "Extended VIP"
}
```

**The field is absent when no mix was chosen.** There is no placeholder value — an entry that just plays the track's primary audio simply has no `selected_mix` key. Treat a missing field as "play the default audio", and never write a stand-in like `"default"`: a player reading that back would look for a mix by that name, find nothing, and cache the same audio under a second key.

The chosen mix is also mirrored into the metadata's attributes as a `Selected Mix` trait, so it shows up on NFT marketplaces alongside the other playlist traits. Players read the top-level field first and fall back to the attribute for older playlists, but the track object is the canonical location.

#### Resolved Media Fields (v0.4)

When a playlist is uploaded, these fields are automatically resolved from the track's metadata. They provide direct access to the best audio and artwork URLs without needing to parse the metadata JSON:

* `audio_url` - Gateway-resolved URL for the best audio (e.g., `https://arweave.net/abc123`). Same field name as the metadata-interior audio URL — when present on the wrapper, it overrides any value found inside `metadata`.
* `artwork_url` - Gateway-resolved URL for the best artwork image. This is the name ApeTapes writes onto the wrapper. Third-party players using the `playlist-data-engine` will see this value exposed as `image_url` on the parsed `PlaylistTrack` — the engine accepts `artwork_url` on input and normalizes it to `image_url` (which pairs with `image_thumb_url`).
* `audio_ipfs_hash` - IPFS CID of the optimized audio file
* `artwork_ipfs_hash` - IPFS CID of the artwork/image file

The URL resolution uses priority queues to pick the best streaming-optimized option from the metadata's audio and image fields. This makes it easy for third-party players to access the audio and artwork without needing to parse the full metadata JSON themselves.

#### Mint Fields (v0.4)

Mint metadata is **NOT** stored on the track wrapper. The `mint_function`, `mint_price`, `mint_snapshot_time`, and `mint_token` fields live only inside the stringified `metadata` interior (the `AudioMetadata` shape produced by the Metadata Maker). They are never promoted onto the track wrapper and never emitted as Arweave tags.

To read mint info for a track, parse the `metadata` field and read the snake_case keys directly:

```typescript
const metadata = JSON.parse(track.metadata);
const mintFunction = metadata.mint_function;   // e.g. "mint"
const mintPrice    = metadata.mint_price;       // wei
const mintToken    = metadata.mint_token;       // ERC20 token address
```

These fields are supported in the type system but have no UI yet, so they remain dormant until a Metadata Maker form populates them.

### The Metadata Field: Where the Magic Happens

The `metadata` field contains stringified JSON with the actual audio files and detailed track information. This is what players parse to find the audio URLs, artwork, lyrics, and other rich content.

**Next:** [Track Metadata →](track-metadata.md) - Dive into what's inside that stringified metadata field.
