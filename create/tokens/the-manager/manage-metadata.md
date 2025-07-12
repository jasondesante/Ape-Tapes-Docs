# Manage Metadata

The metadata links are made up of two parts: the Base URI, and the path. &#x20;

The path is the Token or Contract URI.

For info on what a metadata file is, [click here](../../the-metadata-maker/concepts/what-is-a-metadata-file.md).

In the Manager page you can set the metadata for everything.  Set the Base URI, Contract URI. Add or change any amount of songURIs.

#### Setting Metadata

Setting metadata requires two steps.  The first step is to set the Base URI.  This is a one time thing.  Step two is set the path of the contract/token URI.  Combined these pieces make up the result of a contractURI or tokenURI call.

The metadata maker lets you create a manifest which lets you use the Base URI to be more efficient.  [Read more](../../the-metadata-maker/)

## Base URI

The Base URI is the common part of metadata links.  It's used to reduce gas when creating new songs by splitting the metadata links into two parts, the Base URI and the rest of it.

Base URI + Token/Contract URI = Finished Metadata

You can view and set the Base URI on the Manager page.

If you created a manifest in the Metadata Maker page, you can use that while setting the Base URI.  If the manifest you want to use was the most recent one you created, it should give you a button to set the newly created manifest as the Base URI without having to enter anything manually.

### Why Do I Need A "Base URI"??

* More efficient
* Better organized
* 1 of 2 parts that make up a metadata link

## Contract Metadata

Base URI + Contract URI = Contract Metadata

The Contract URI is a link to the contract metadata file.  The contract metadata file is a json object which contains all sorts of information like the description of the contract, images, and more.

You can view the contract metadata on the Manager page.  You can set the Contract URI.  It is important that you set a Contract URI to your contract.  Without a profile image, it won't properly show up in the browser.

## Add / Edit Any Metadata

Base URI + Token URI = Token Metadata

You can add/edit metadata files to any rarity of a song after it has been created. &#x20;

You can edit multiple rarities of metadata in one transaction.  You can edit multiple songs and multiple rarities in one transaction.  You can fix mistakes in the token URIs, or enhance the amount of rarities.

