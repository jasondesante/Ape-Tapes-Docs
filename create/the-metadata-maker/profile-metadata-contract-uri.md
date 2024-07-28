# Profile Metadata (contract URI)

The Profile Metadata Maker gathers the pictures, description, important links and more for your record label. &#x20;

### Automatic IPFS Links

The IPFS link shows up when you add any file.  You'll have the option later to upload to Arweave.

### contractURI Function

The profile metadata is what shows up when you use the contractURI function on your smart contract.  It's set with the setContractURI function. &#x20;

## Input Fields

### Required

The required fields in the Profile Metadata Maker are: &#x20;

* Name
* Image
* Banner Image

### Optional

The other fields are optional for the contract uri.  Even the description is optional.  It's recommended to write in a description though!  Other optional fields for contract metadata include the bonus images array, and links for all social medias.  Like "spotify\_url"



## Creating Metadata

Making metadata is easy.  First thing is to gather your files.  Fill out the required fields.  Fill out as many optional fields as you want.  Now you're ready for the next step.

## Saving

Click save when you're finished adding files.  [Add a license](add-license.md), upload to Arweave, or skip and use IPFS. &#x20;

It's highly recommended to upload your files to Arweave. To do that you'll need to have a balance on [Irys](./#irys) larger than the price. You can deposit to the [Irys](./#irys) contract with the button in the details.

Once you sign, the files are uploaded.  The IPFS links are replaced with the new Arweave links, and the metadata file is created. &#x20;

### Downloading

You will then see a button to download the file, as well as the IPFS link to the finished metadata.

There's also the option to download the raw metadata which is a bigger file that's better suited to import back into the metadata maker later.



Now you're done creating the profile metadata!



