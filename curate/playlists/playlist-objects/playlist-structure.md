# Playlist Structure

The playlist structure defines the outer container that holds all tracks and playlist-level information.

### Core Playlist Fields

Every playlist contains these essential elements that describe the collection as a whole:

json

```json
{
  "type": "Serverless-Playlist",
  "name": "House Jams - Spinamp", 
  "description": "Originally created on Spinamp.xyz\nCreated by Eva Myra May",
  "genre": "House",
  "tags": ["spinamp", "eva myra may", "house"],
  "image": "https://arweave.net/vMOPd7UKmBR20pItrgIFIb9RgU57poiP3eQqYokevE0",
  "creator": "0x44b32db7c365d99ee8a5d5cc28875ad2008813e0",
  "version": "0.3",
  "tracks": [...],
  "nextIndex": 6
}
```

### Field Descriptions

| Field         | Type   | Description                   |
| ------------- | ------ | ----------------------------- |
| `type`        | String | Always "Serverless-Playlist"  |
| `name`        | String | Playlist title                |
| `description` | String | Playlist description          |
| `genre`       | String | Musical genre classification  |
| `tags`        | Array  | Discovery and search tags     |
| `image`       | String | Playlist artwork URL          |
| `creator`     | String | Wallet address of creator     |
| `version`     | String | Metadata format version       |
| `tracks`      | Array  | Collection of track objects   |
| `nextIndex`   | Number | Next available track position |

### The Tracks Array

The `tracks` field contains an array of track objects. Each entry in this array represents one piece of music that can be played. This is where the actual content lives - the playlist structure just organizes and describes the collection.

**Next:** [Track Objects →](track-objects.md) - Learn what's inside each entry in the tracks array.
