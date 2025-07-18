---
description: These are the tags that audio files have
---

# Audio Tags

Every audio file is tagged this way with the default and custom tags. This ensures a nice base layer of discoverability. Every audio file gets these tags, whether they are uploaded with the audio uploader or in a bundle with the metadata maker.

## Default Tags

Every audio file uploaded with The Contract Wizard has these tags added to them:

`App-Name:Contract-Wizard`

`Uploaded-Type:Audio`

`IPFS-CID:`(ipfs content id)

`Uploaded-By:`(wallet that uploaded)

## **Custom Tags**

Right now there are 5 audio tags written by the user:

`Title:`(title)

`Artist:`(artist)

`Genre:`(genre)

`ISRC:`(isrc code)

`Audio-Tag:`(audio tag)

There's only ever one Title, Artist, Genre, and ISRC tag, but there can be multiple Audio-Tag tags.

[Here](https://viewblock.io/arweave/tx/BDhxHebKarvMgDtM5t7fX2S6eGGroRF_7NLFgQ7ixgE) is an example of a published audio file's tags.

### **Query Audio Data**

You can query different tags directly at ar://listen with the [Arweave Explorer](../../../consume/discover/the-browse-page/arweave-explorer.md) page.

{% embed url="https://listen.arweave.net/#/arweave-explorer" %}

You can also do a query on other sites and see what happens when you search App-Name: Contract-Wizard, or Uploaded-Type: Audio, or any of the other tags.

{% embed url="https://arweave-search.goldsky.com/graphql" %}

## **Audio Tags Explained**

**Uploaded-Type: The File Category** The most important tag for searching. For audio uploads, this is always "Audio" to distinguish from playlists, metadata, and manifests.

### **System Tags (Always the Same)**

**App-Name** - Always "Contract-Wizard" to show what app uploaded the file

**Audio-Version** - Always "0.3" for the current audio metadata version

**IPFS-CID** - The IPFS content ID for permanent pinning

**Uploaded-By** - The wallet address of the uploader

### **User-Controlled Tags**

**Title** - The name of your track

**Artist** - The performing artist

**Genre** - Musical genre you assign

**ISRC** - International Standard Recording Code for the track

**Audio-Tag** - Custom tags for discovery

