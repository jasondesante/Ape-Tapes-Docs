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
  "audioUrl": "https://arweave.net/abc123...",
  "artworkUrl": "https://arweave.net/def456...",
  "audioIpfsHash": "Qm...",
  "artworkIpfsHash": "Qm..."
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

#### Resolved Media Fields (v0.4)

When a playlist is uploaded, these fields are automatically resolved from the track's metadata. They provide direct access to the best audio and artwork URLs without needing to parse the metadata JSON:

* `audioUrl` - Gateway-resolved URL for the best audio (e.g., `https://arweave.net/abc123`)
* `artworkUrl` - Gateway-resolved URL for the best artwork image
* `audioIpfsHash` - IPFS CID of the optimized audio file
* `artworkIpfsHash` - IPFS CID of the artwork/image file

The URL resolution uses priority queues to pick the best streaming-optimized option from the metadata's audio and image fields. This makes it easy for third-party players to access the audio and artwork without needing to parse the full metadata JSON themselves.

#### Mint Fields (v0.4)

Optional fields for tracks that represent mintable tokens:

* `Mint-Function` - Preferred mint function name (e.g., "mint", "mintCopy")
* `Mint-Price` - Mint price in wei
* `Mint-Snapshot-Time` - Unix timestamp of when mint info was captured
* `Mint-Token` - ERC20 token address for alternative payment (e.g., USDC)

These fields are supported in the type system and stored in the JSON body, but do not have UI yet. When metadata containing these fields is used in a playlist, the values are automatically promoted to the top-level track fields.

### The Metadata Field: Where the Magic Happens

The `metadata` field contains stringified JSON with the actual audio files and detailed track information. This is what players parse to find the audio URLs, artwork, lyrics, and other rich content.

**Next:** [Track Metadata →](track-metadata.md) - Dive into what's inside that stringified metadata field.
