---
description: New and improved! Try it now!
---

# Manifest Maker

This page is where you upload all the metadata files for your collection into one folder. &#x20;

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-17 at 2.59.32 AM.png" alt=""><figcaption></figcaption></figure>

## Creating A Manifest

#### Step 1 - Import/Create

Making a manifest is easy.  First name your folder and choose to create a new manifest or import an existing manifest to upgrade it. &#x20;

Clicking "Import Existing Manifest" opens the file picker and shows your manifests so you can choose which collection to upgrade.

***

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-17 at 3.32.05 AM.png" alt=""><figcaption></figcaption></figure>

#### Step 2 - Select Files

Add files from your computer by dragging and dropping the files into the box, or click the box to bring up a menu. &#x20;

Click the "Select Metadata Files" button to open the File Picker and choose already uploaded metadata, as well as locally saved metadata that has yet to be uploaded.

You can replace metadata files if you imported an existing folder. This is very awesome and simplifies upgrading an existing collection by a lot of steps. &#x20;

Prepare all your metadata files.  Add them in the order you want.  Don't add them in a random order.

***



#### Step 3 - Configure Manifest

Review the files, make sure you're cool with the ordering.  Make sure you got enough in your balance.  Then upload the metadata to create your manifest.

## Saving

Click the upload button and sign.  Now the metadata for your collection is uploaded.





#### Step 4 - Upload Complete





### Downloading

Once your manifest is uploaded to Arweave you'll see a link for the index, with the file name of the manifest id.

The index is a handy file showing you the name of every file you uploaded.  You can use the index to see the file name corresponding with each path. &#x20;

To get to each file you add the path to the manifest.  You can see that when viewing the index link because the index's path is "index", and what comes before it is the manifest transaction id.  It's recommended to download and bookmark the index and manifest.



### Metadata Functions

For contract owners, when you're done creating the manifest, the next step is to set the Base URI.

The manifest is what will return at the baseURI function on your smart contract.  It's set with the setBaseURI function.  By putting the manifest in the baseURI, you reduce the amount of characters needed to enter for each tokenURI.
