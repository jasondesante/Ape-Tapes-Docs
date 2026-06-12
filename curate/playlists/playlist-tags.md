---
description: These are the tags that playlists have
---

# Playlist Tags

This is detailing the Arweave tags for the playlists.  These are all the tags that are put onto the playlist file that are queryable on chain tags.

View an example of a playlist's tags [here](https://viewblock.io/arweave/tx/h_e_Y7Ea2hg2XCOuA6E-LHpGa8LDL3My7blT44vPkhU).&#x20;

## Default Tags

Every playlist uploaded with The Contract Wizard has these tags added to them:

* `App-Name:Contract-Wizard`
* `Playlist-Version: 0.4`
* `Uploaded-Type:Playlist`
* `IPFS-CID:`(ipfs content id)
* `Uploaded-By:`(wallet that uploaded)

The most important is **Uploaded-Type:Playlist**. Make sure you write that exactly, as that tag is how all playlists are queried.

## Custom Tags

Right now there are up to 6 playlist tags written by the user:

* `Title:`(title)
* `Genre:`(genre)
* `Search-Tag:`(searchable tag)
* `Playlist-Type:`(playlist type)
* `Artist:`(artist name — for ep/lp/single types)
* `Image:`(arweave transaction id)

There can be multiple Search-Tag tags but only one Genre tag. **Remember** to [convert everything to lowercase](playlist-tags.md#importance-of-lower-case-tags) so it's easier to search.

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
* **Playlist-Version** - Currently "0.4" for the playlist metadata version
* **IPFS-CID** - The IPFS content ID for permanent pinning
* **Uploaded-By** - The wallet address of the uploader

### **User-Controlled Tags (lower case values)**

* **Title** - The name you give your playlist
* **Genre** - Musical genres you assign
* **Search-Tag** - Unified searchable tags for discovery. The playlist Title, Genre, and any custom tags are all stored as `Search-Tag` entries so a single query matches everything.
* **Playlist-Type** - The type of playlist (see below)
* **Artist** - The artist name (included when Playlist-Type is ep, lp, or single)
* **Image** - Optional cover art as a raw Arweave transaction ID (no `ar://` prefix)

### Playlist-Type

The `Playlist-Type` tag classifies what kind of playlist it is. It replaces the old "Remix" tag with more specific values:

| Value | Description | Additional Tags |
|-------|-------------|-----------------|
| `new` | Default — a new original playlist | None |
| `remix` | A remix of an existing playlist | `Original-Playlist` (tx_id of original) |
| `ep` | Extended Play release | `Artist` (artist name) |
| `lp` | Long Play release | `Artist` (artist name) |
| `single` | Single track release | `Artist` (artist name) |

When the type is `remix`, an additional tag called `Original-Playlist` is added with the Arweave transaction ID of the original playlist.

When the type is `ep`, `lp`, or `single`, an `Artist` tag is added with the artist name (also duplicated as a `Search-Tag`).

### **Search-Tag: Unified Search**

The `Search-Tag` tag works the same way as it does for audio files. When a playlist is uploaded, the following values are all stored as `Search-Tag` entries:

* The playlist **Title**
* The **Genre**
* Any **custom tags** entered by the user
* The **Artist** name (when the playlist type is ep, lp, or single)

This means you can search `Search-Tag` with a single query and match against all of these values at once.

#### Importance of Lower Case Tags

Every user controlled tag gets turned into lower case so it's easier to search. If this wasn't done then "rock" and "Rock" would be treated as different genres, so it's best to convert any capitals into lower case so there's no confusion when searching those tags. This makes it easier to query the tags on Arweave and prevents mistakes.

If you write your custom tags in lower case:

* Searching is twice as fast.
* Easier for other builders to implement.&#x20;
* More likely to show up in search results.

For the full breakdown of why lowercase matters and all tagging conventions, see [Tagging Best Practices →](../../../create/build-your-vision/tagging-best-practices.md).

### Ready To Build

You can build your own site to listen to playlists, create new ones, or curate the existing library of playlists to find the best ones. The possibilities are endless!

These tags are made to create a shared library of files that can be easily searched and shared across decentralized apps. This is open for anyone to contribute to with their tagged files or by curating the growing archive.&#x20;

When building your own uploader/tagger, for the most efficient tagging don't forget "**Uploaded-Type:Playlist**" to contribute to the library.
