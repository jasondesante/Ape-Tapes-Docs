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
  "version": "0.4",
  "playlist_type": "new",
  "tracks": [...],
  "next_index": 6
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
| `version`     | String | Metadata format version (currently "0.4") |
| `tracks`      | Array  | Collection of track objects   |
| `next_index`  | Number | Next available track position |

### Playlist Type Fields (v0.4)

These optional fields classify the playlist type and provide additional metadata:

| Field                    | Type   | Description                                                  |
| ------------------------ | ------ | ------------------------------------------------------------ |
| `playlist_type`          | String | Type classification: "new", "remix", "ep", "lp", or "single" |
| `original_playlist_tx_id`| String | For remixes — Arweave tx_id of the original playlist        |
| `playlist_artist`        | String | For ep/lp/single — artist name                              |
| `platform`               | String | Origin platform for directory-imported playlists. Currently `"contract-wizard"` (CW v0.3 → v0.4 migration) or `"nina"` (Nina multi-format split). Absent on user-created playlists. |

See [Playlist Tags](../playlist-tags.md#playlist-type) for how these map to on-chain tags.

### The Tracks Array

The `tracks` field contains an array of track objects. Each entry in this array represents one piece of music that can be played. This is where the actual content lives - the playlist structure just organizes and describes the collection.

**Next:** [Track Objects →](track-objects.md) - Learn what's inside each entry in the tracks array.
