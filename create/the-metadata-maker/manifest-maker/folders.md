---
description: aka Manifests
---

# Folders

A "manifest" is a shared link for all the files.  Saving lots of gas, and simplifying the urls.

For Arweave, a "manifest" is a special file that defines a folder structure by listing multiple files. You can access any file within the manifest by combining the manifest's transaction ID (tx\_id) with the specific file's path. This allows you to group multiple files under a shared URL, with each file accessible via its unique path.

### Rules For NFTs

In the context of "The Manifest Maker", that tool creates a specific type of manifest that includes only JSON metadata files meant to be used as the baseURI for an NFT collection.

For NFT Collections the suggested way to create links is to set a long baseURI and short path for each token, so the unique parts of the tokenURI are kept to a minimum.  This maximizes efficiency and minimizes gas. You set the gateway + manifest tx\_id as the baseURI and the file path as the token path.

### File URLs

For Arweave manifests, the url can be thought of like this:

gateway (ar:// or arweave.net/) + manifest tx\_id + file path = file url

In the context of NFTs it can be framed like this:

baseURI + token path = tokenURI

