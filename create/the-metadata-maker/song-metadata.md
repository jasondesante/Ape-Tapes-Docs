# Song Metadata

The Song Metadata Maker gathers the audio file, pictures and everything else to create magic like you've never seen before.

### Metadata Functions

Set the metadata with setSongURI function, or when an original is created.  &#x20;

View the metadata with the tokenURI or songURI functions on your smart contract. &#x20;

### Automatic IPFS

Before you upload to Arweave, newly added files will show the IPFS link in their url fields. You'll have the option later to upload to Arweave.

## Input Fields

### Required

The required fields in the Song Metadata Maker are: &#x20;

* Title
* Artist
* Audio
* Image

### Optional

The other fields are optional for the Song URI.  Some optional fields for song metadata include:

* Album
* Track Number
* Collaborating Artists
* Artist Image
* Album Image
* [ISRC](metadata-standards/token-metadata/noteworthy-traits.md#isrc)
* UPC
* [Lyrics](song-metadata.md#lyrics)
* [Genres](metadata-standards/token-metadata/noteworthy-traits.md#genre-tags)
* [Tags](metadata-standards/token-metadata/noteworthy-traits.md#genre-tags)
* Description
* [Song (Lossy, Mp3)](metadata-standards/token-metadata/noteworthy-traits.md#audio)
* [Video](metadata-standards/token-metadata/noteworthy-traits.md#video)
* [Visualizer](metadata-standards/token-metadata/noteworthy-traits.md#visualizer)
* [Clone Hero Charts](metadata-standards/token-metadata/noteworthy-traits.md#clone-hero)
* [Step Mania Charts](metadata-standards/token-metadata/noteworthy-traits.md#step-mania)
* [VRM (Avatar)](metadata-standards/token-metadata/noteworthy-traits.md#vrm)
* [Merch (3D Model)](metadata-standards/token-metadata/noteworthy-traits.md#merch)
* [Midi](metadata-standards/token-metadata/noteworthy-traits.md#midi)

Additional categories of metadata that unlock new functionality are:

* [Attributes](metadata-standards/token-metadata/grouped-traits.md#attributes)
* [Credits](metadata-standards/token-metadata/grouped-traits.md#credits)
* [Stems](metadata-standards/token-metadata/grouped-traits.md#stems)
* [Mixes](metadata-standards/token-metadata/grouped-traits.md#mixes)



## Creating Metadata

Making metadata is easy.  First thing is to gather your files.  Fill out the required fields.  Fill out as many optional fields as you want.  Now you're ready for the next step.

## Saving

Click save when you're finished adding files.  [Add a license](concepts/adding-licenses.md), upload to Arweave, or skip and use IPFS.

It's highly recommended to upload your files to Arweave. To do that you'll need to have a balance on [Irys](./#irys) larger than the price. You can deposit to the [Irys](./#irys) contract with the button in the details.

Once you sign, the files are uploaded.  The IPFS links are replaced with the new Arweave links, and the metadata files are created. &#x20;

### Downloading

You will then see a button to download every rarity in a zip, as well as the IPFS links to the finished metadata.

There's also the option to download the raw metadata.  The raw file is there to recover as a save state when updating the metadata later.  One reason the raw is best for updating is the rarities are in the one file.



Now you're done creating the song metadata!
