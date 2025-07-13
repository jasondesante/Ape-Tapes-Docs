# Playlist Objects

A playlist file is a JSON object containing an array of track objects. Each track represents a piece of music that can be played across the decentralized web.

View live playlist example [→](https://arweave.net/ubK7Ona9YZz6aHNvfzvD61xBG4cfutvVpM9OyamFKtU)

## Inside A Playlist Object

### Structure Overview

Every playlist contains these core elements:

* **Metadata**: Name, description, genre, tags, creator info
* **Tracks Array**: Collection of music tokens and files
* **Version Control**: Tracking format changes over time



## 📋 Complete Playlist Object

```json
// Example playlist object
{
  "type": "Serverless-Playlist",
  "name": "House Jams - Spinamp",
  "tracks": [
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
    },
    ...
  ],
  "nextIndex": 6,
  "description": "Originally created on Spinamp.xyz\nCreated by Eva Myra May",
  "genre": "House",
  "tags": ["spinamp", "eva myra may", "house"],
  "image": "https://arweave.net/vMOPd7UKmBR20pItrgIFIb9RgU57poiP3eQqYokevE0",
  "creator": "0x44b32db7c365d99ee8a5d5cc28875ad2008813e0",
  "version": "0.3"
}
```

| Field         | Type   | Description                   |
| ------------- | ------ | ----------------------------- |
| `type`        | String | Always "Serverless-Playlist"  |
| `name`        | String | Playlist title                |
| `tracks`      | Array  | Collection of track objects   |
| `nextIndex`   | Number | Next available track position |
| `description` | String | Playlist description          |
| `genre`       | String | Musical genre classification  |
| `tags`        | Array  | Discovery and search tags     |
| `image`       | String | Playlist artwork URL          |
| `creator`     | String | Wallet address of creator     |
| `version`     | String | Metadata format version       |

## 🎵 Track Objects

#### Track Object Fields

**Essential Fields:**

* `metadata` - Stringified JSON containing audio links and track info
* `title` - Track name
* `playlist_index` - Position in playlist
* `uuid` - Unique identifier for duplicate handling

**Token Fields (when track is an NFT):**

* `chain_name` - Blockchain network
* `token_address` - Contract address
* `token_id` - Token identifier
* `platform` - Minting platform
* `contract_type` - Contract standard

**Technical Fields:**

* `id` - A unique identifier for each track
* `token_uri` - Metadata URL
* `name` - Contract name
* `symbol` - Contract symbol



## 📝 Track Metadata Structure

The track can be a token or a file.  The track's metadata is it's own object which is then stringified when put into the larger track object.

### **Adding A Token**

It probably follows nft metadata standards (like [opeasea](https://docs.opensea.io/docs/metadata-standards)). The most important thing is if the token has audio in it or not.  The audio will be checked at the most standard field "animation\_url" and then also "audio\_url", "lossless\_audio", "mp3\_url", and "lossy\_audio". If nothing is found in those fields in the stringified object in the metadata field then it won't show up in the player.  The player only shows tokens that have something in those fields.

### **Adding A File**&#x20;

It won't follow any metadata standards.  Tracks in playlists fall anywhere in the spectrum from undocumented file to thicc metadata, and it's when the file is added that it's formatted like metadata so everything all works. What happens is the raw file gets put into an object into the field "animation\_url", to the same standards as an NFT metadata. But it's just a normal file with some extra info.&#x20;

A file that's added to a playlist will have a json objected created when it's added.

If the track is a metadata file then it already has been prepared correctly and is then turned into a string and added to the metadata field.

Track metadata follows the ultimate bedrock of nft metadata standards the [opensea metadata standards](https://docs.opensea.io/docs/metadata-standards). That is where "animation\_url" comes from, among other stuff.

The closer it is to [thicc metadata](../../create/the-metadata-maker/metadata-standards/token-metadata.md) the better.

