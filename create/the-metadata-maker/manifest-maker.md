# Manifest Maker

The manifest is a shared link for all the files.  Saving lots of gas, and simplifying the urls.

Clicking "Update Collection" will take you to the manifest maker.  This page is where you upload all the metadata files for your collection into one folder. &#x20;

### baseURI Function

The manifest is what will show as the baseURI function on your smart contract.  It's set with the setBaseURI function.  By putting the manifest in the baseURI, you reduce the amount of characters needed to enter for each tokenURI.

### JSON Files Only

The only files accepted on this page are metadata json files and zips that have json files in them.  The zip support is because the song metadata maker outputs a zip when you create many rarities.  So it's easier to add all the rarities for the song at once as a zip rather than unzip and add all the separate json files.  We're trying to make things easy while keeping the customization and openness.&#x20;



## Creating A Manifest

Making a manifest is easy.  Prepare all your metadata files.  Add them in the order you want.  Don't add them in a random order.

Review the files, make sure you're cool with the ordering.  Make sure you got enough in your Irys balance.  Then upload the metadata to create your manifest.

## Saving

Click the upload button and sign.  Now the metadata for your collection is uploaded.

### Downloading

Once your manifest is uploaded to Arweave you'll see a link for the index, with the file name of the manifest id.

The index is a handy file showing you the name of every file you uploaded.  You can use the index to see the file name corresponding with each path. &#x20;

To get to each file you add the path to the manifest.  You can see that when viewing the index link because the index's path is "index", and what comes before it is the manifest transaction id.  It's recommended to download and bookmark the index and manifest.



Now you're done creating the manifest!  The next step is to set the manifest as the Base URI.
