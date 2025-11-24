---
description: On chain and searchable.
---

# Audio Tags

Every audio file gets tagged when it's uploaded. This ensures a base layer of discoverability. Every audio file gets tagged whether they're uploaded with the audio uploader or in a bundle with The Metadata Maker.

## Default Tags

Every audio file uploaded has these tags added to them:

`App-Name:Contract-Wizard`

`Uploaded-Type:Audio`

`IPFS-CID:`(ipfs content id)

`Uploaded-By:`(wallet that uploaded)

The most important tag when uploading audio or metadata, is "**Uploaded-Type:Audio**". This gives a common tag to both audio files and audio metadata, letting them both show up with one query.&#x20;

## **Custom Tags**

Custom tags are written by the user. Right now there are 5 optional audio tags:

`Title:`(title)

`Artist:`(artist)

`Genre:`(genre)

`ISRC:`(isrc code)

`Audio-Tag:`(audio tag)

There's only ever one Title, Artist, Genre, and ISRC tag, but there can be multiple Audio-Tag tags. **Remember** to [convert everything to lowercase](audio-tags.md#importance-of-lower-case-tags) so it's easier to search.

[Here](https://viewblock.io/arweave/tx/BDhxHebKarvMgDtM5t7fX2S6eGGroRF_7NLFgQ7ixgE) is an example of a published audio file's tags.

### **Query Audio Data**

You can query different tags directly at ar://listen with the [Arweave Explorer](../../../consume/discover/the-browse-page/arweave-explorer.md) page.

{% embed url="https://listen.arweave.net/#/arweave-explorer" %}

You can also do a query on other sites and see what happens when you search App-Name: Contract-Wizard, or Uploaded-Type: Audio, or any of the other tags.

{% embed url="https://arweave-search.goldsky.com/graphql" %}

## **Audio Tags Explained**

**Uploaded-Type:Audio** The most important tag for searching. For audio uploads, this is always "Audio" to distinguish from playlists, and manifests. The "Audio" value is capitalized because it is a value that will never change.

### **System Tags (Always the Same)**

**App-Name** - Always "Contract-Wizard" to show what app uploaded the file

**Audio-Version** - Always "0.3" for the current audio metadata version

**IPFS-CID** - The IPFS content ID for permanent pinning

**Uploaded-By** - The wallet address of the uploader

### **User-Controlled Tags (lower case except ISRC)**

**Title** - The name of your track

**Artist** - The performing artist

**Genre** - Musical genre you assign

**Audio-Tag** - Custom tags for discovery

**ISRC** - International Standard Recording Code for the track (case sensitive)

#### Importance of Lower Case Tags

Every value in a user controlled tag gets turned into lower case, so it's easier to search. ISRC is the exception because it's an exact code. If this wasn't done then "rock" and "Rock" would be treated as different genres, so it's best to convert any capitals into lower case so there's no confusion when searching those tags.

If you write your custom tags in lower case:

* Searching the file takes half the work, is twice as fast.
* Easier for other builders to implement.&#x20;
* More likely to show up in search results.

### Ready To Build

These tags are made to create a shared library of files that can be easily searched and shared across decentralized apps. This is open for anyone to contribute to with their tagged files or by curating the growing archive.&#x20;

When building your own uploader/tagger, for the most efficient tagging don't forget "**Uploaded-Type:Audio**" for audio files and audio metadata.

