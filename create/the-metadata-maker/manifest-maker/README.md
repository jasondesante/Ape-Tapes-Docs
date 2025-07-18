---
description: New and improved! Try it now!
---

# Manifest Maker

This page is where you upload all the metadata files for your collection into one folder. &#x20;

## Creating A Manifest

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-17 at 2.59.32 AM.png" alt=""><figcaption></figcaption></figure>

### Step 1 - Import/Create

Making a manifest is easy.  First name your folder and choose to create a new manifest or import an existing manifest to upgrade it. &#x20;

Clicking "Import Existing Manifest" opens the file picker and shows your manifests so you can choose which collection to upgrade.

***

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-17 at 3.32.05 AM.png" alt=""><figcaption></figcaption></figure>

### Step 2 - Select Files

Add files from your computer by dragging and dropping the files into the box. &#x20;

Click the "Select Metadata Files" button to open the File Picker and choose already uploaded metadata, as well as locally saved metadata that still needs to be uploaded.

You can replace metadata files if you imported an existing folder. This is very awesome and simplifies upgrading an existing collection by a lot of steps. &#x20;

***

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-17 at 11.22.28 PM (1).png" alt=""><figcaption></figcaption></figure>

### Step 3 - Configure Manifest

Review the files, make sure you're cool with the ordering.  Manifests are small so you should have enough credits in your balance to upload.&#x20;

In the "Options" tab you have buttons to download a numbered list of the files so you can more easily keep track of the manifest's file order. There's also an option to make the paths in the manifest be numbers or the original file names.  When the path is a number it's way less characters than the file names.  The default is to rename all the file paths to numbers because The Manifest Maker is meant to create folders for NFT collections, and you save a lot of gas when writing shorter tokenURIs.

Once you're ready click upload and sign. The new files will be uploaded along with the manifest file detailing the folder structure.

***

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-17 at 11.21.19 PM.png" alt=""><figcaption></figcaption></figure>

### Step 4 - Upload Complete

Now the metadata for your collection is uploaded into one folder. You have some buttons suggesting what to do next:

* **Update Collection** - You can go straight to The Contract Manager to update your collection.
* **View Manifest** - View the index of your new folder to see the list of files and their paths.
* **Library** - Goes to the Arweave Uploads Page. Notice how uploaded local metadata files now say "uploaded", letting you know they're safe to delete.

It's recommended to download and bookmark the index and manifest url.

### Metadata Functions

For contract owners, when you're done creating the manifest, the next step is to set the Base URI.

The manifest is what will return at the baseURI function on your smart contract.  It's set with the setBaseURI function.  By putting the manifest in the baseURI, you reduce the amount of characters needed to enter for each tokenURI.
