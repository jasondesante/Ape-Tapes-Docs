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
  "playlist_index": 1
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

### The Metadata Field: Where the Magic Happens

The `metadata` field contains stringified JSON with the actual audio files and detailed track information. This is what players parse to find the audio URLs, artwork, lyrics, and other rich content.

**Next:** [Track Metadata →](track-metadata.md) - Dive into what's inside that stringified metadata field.
