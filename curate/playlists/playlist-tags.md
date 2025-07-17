---
description: These are the tags that playlists have
---

# Playlist Tags

This is detailing the Arweave tags for the playlists.  These are all the tags that are put onto the playlist file that are queryable on chain tags.

View an example of a playlist's tags [here](https://viewblock.io/arweave/tx/h_e_Y7Ea2hg2XCOuA6E-LHpGa8LDL3My7blT44vPkhU).&#x20;

## Default Tags

Every playlist uploaded with The Contract Wizard has these tags added to them:

* App-Name:Contract-Wizard
* Playlist-Version: 0.3
* IPFS-CID:(ipfs content id)
* Uploaded-Type:Playlist
* Uploaded-By:(wallet that uploaded)

## Custom Tags

Right now there are 3 playlist tags written by the user:

* Title:(title)
* Genre:(genre)
* Audio-Tag:(audio tag)

There's only ever one Genre tag but there can be multiple Audio-Tag tags.

[Here](https://viewblock.io/arweave/tx/4WCirOpvoCEOa_SwBqzyyxSXIBmSQ6kfkfAEueXa0IQ) is an example of a published playlist's tags.

### Query Playlist Data

You can query different tags directly at ar://listen with the [Arweave Explorer](../../consume/discover/the-browse-page/arweave-explorer.md) page.

{% embed url="https://listen.arweave.net/#/arweave-explorer" %}

You can also do a query on other sites and see what happens when you search App-Name: Contract-Wizard, or any of the other tags. &#x20;

{% embed url="https://arweave-search.goldsky.com/graphql" %}

## Playlist Tags Explained

**Uploaded-Type: The File Category** The most important tag for searching. For playlist uploads, this is always "Playlist" to distinguish from audio, metadata, and manifests.

### **System Tags (Always the Same)**

* **App-Name** - Always "Contract-Wizard" to show what app uploaded the file
* **Playlist-Version** - Always "0.3" for the current playlist metadata version
* **IPFS-CID** - The IPFS content ID for permanent pinning
* **Uploaded-By** - The wallet address of the uploader

### **User-Controlled Tags**

* **Title** - The name you give your playlist
* **Genre** - Musical genres you assign
* **Audio-Tag** - Custom tags for discovery
