---
description: These are the tags that playlists have
---

# Playlist Tags

This is detailing the Arweave tags for the playlists.  These are all the tags that are put onto the playlist file that are queryable on chain tags.

View an example of a playlist's tags [here](https://viewblock.io/arweave/tx/h_e_Y7Ea2hg2XCOuA6E-LHpGa8LDL3My7blT44vPkhU).&#x20;

## Default Tags

Every playlist uploaded with The Contract Wizard has these tags added to them:

* `App-Name:Contract-Wizard`
* `Playlist-Version: 0.3`
* `Uploaded-Type:Playlist`
* `IPFS-CID:`(ipfs content id)
* `Uploaded-By:`(wallet that uploaded)

The most important is **Uploaded-Type:Playlist**. Make sure you write that exactly, as that tag is how all playlists are queried.

## Custom Tags

Right now there are 3 playlist tags written by the user:

* `Title:`(title)
* `Genre:`(genre)
* `Audio-Tag:`(audio tag)

There can be multiple Audio-Tag tags but only one Genre tag. Remember to [convert everything to lowercase](playlist-tags.md#importance-of-lower-case-tags) so it's easier to search.

[Here](https://viewblock.io/arweave/tx/4WCirOpvoCEOa_SwBqzyyxSXIBmSQ6kfkfAEueXa0IQ) is an example of a published playlist's tags.

### Query Playlist Data

You can query different tags directly at ar://listen with the [Arweave Explorer](../../consume/discover/the-browse-page/arweave-explorer.md) page.

{% embed url="https://listen.arweave.net/#/arweave-explorer" %}

You can also do a query on other sites and see what happens when you search App-Name: Contract-Wizard, or any of the other tags. &#x20;

{% embed url="https://arweave-search.goldsky.com/graphql" %}

## Playlist Tags Explained

**Uploaded-Type:Playlist** The most important tag for searching. For playlist uploads, this is always "Playlist" to distinguish from audio, metadata, and manifests. The "Playlist" value is capitalized because it is a value that will never change.

### **System Tags (Always the Same)**

* **App-Name** - Always "Contract-Wizard" to show what app uploaded the file
* **Playlist-Version** - Always "0.3" for the current playlist metadata version
* **IPFS-CID** - The IPFS content ID for permanent pinning
* **Uploaded-By** - The wallet address of the uploader

### **User-Controlled Tags (lower case values)**

* **Title** - The name you give your playlist
* **Genre** - Musical genres you assign
* **Audio-Tag** - Custom tags for discovery

#### Importance of Lower Case Tags

Every user controlled tag gets turned into lower case so it's easier to search. If this wasn't done then "rock" and "Rock" would be treated as different genres, so it's best to convert any capitals into lower case so there's no confusion when searching those tags. This makes it easier to query the tags on Arweave and prevents mistakes.

If you write your custom tags in lower case:

* The searching gets literally twice as efficient
* You're more likely to show up on searches
