# Playlist Objects

A playlist file is a JSON object containing an array of track objects. Each track represents a piece of music that can be played across the decentralized web.

View live playlist example [→](https://arweave.net/ubK7Ona9YZz6aHNvfzvD61xBG4cfutvVpM9OyamFKtU)

### What's Inside a Playlist

Every Serverless Playlist contains these core elements:

* **Playlist Metadata**: Name, description, genre, creator info
* **Tracks Array**: Collection of music tokens and files
* **Track Objects**: Individual entries in the tracks array
* **Track Metadata**: Stringified JSON inside each track containing audio links

### Structure Overview

```
Playlist Object
├── name, description, creator, etc.
└── tracks: [
    ├── Track Object 1
    │   ├── title, chain_name, token_address, etc.
    │   └── metadata: "{...stringified track metadata...}"
    ├── Track Object 2
    └── Track Object 3...
]
```

### Learn More

Understanding playlist objects requires diving into three key areas:

[**Playlist Structure →**](playlist-structure.md)\
The outer container with playlist-level information

[**Track Objects →**](track-objects.md)\
Individual entries in the tracks array

[**Track Metadata →**](track-metadata.md)\
The stringified content inside each track object

***

These playlists work anywhere the internet does - no servers required. The more thicc the metadata, the better the experience across different players and platforms.
