# Manage Metadata

Set the Base metadata, Contract metadata, add or change any amount of song metadata files.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-19 at 12.58.52 AM.png" alt=""><figcaption></figcaption></figure>

## Formula For A Link

The metadata links are made up of two parts: the baseURI + the path. &#x20;

The path is either the songURI or contractURI.

#### Setting Metadata

Setting metadata requires two steps.  First set the baseURI for the collection.  Then set the path of the contract/song.  Combined these pieces make up the result of a contractURI or songURI call.

The Manifest Maker lets you create a folder to be used as the baseURI.  [Read more](../../the-metadata-maker/manifest-maker/)

Without a manifest, the baseURI would only be able to include the gateway ("ar://", or "https://arweave.net"), leaving way more characters up to the individual songURIs.  This also means you can't update the entire collection at once.  With manifests, since the paths stay the same across versions if you do it right, you can update the entire collection at once by updating just the baseURI.

## Options

### Base URI

The baseURI is the common part of metadata links.  The metadata links are created by two parts, the baseURI and the path.

baseURI + Song/Contract path = Finished Metadata

You can view and set the baseURI on the Manager page.

If you created a folder with the Manifest Maker, you can set that as the baseURI. Click the "Use Saved Manifest" button to assign the most recently created manifest to your baseURI. You can also manually enter in a baseURI.

### Contract Metadata

baseURI + Contract metadata path = contractURI

The contractURI is a link to the contract metadata file.  The contract metadata is a JSON object which contains information like the description, images, and more. Read about contract metadata standards [here.](../../the-metadata-maker/metadata-standards/contract-metadata.md)

You can view the contract metadata on the Manager page. It's important that you set a contractURI to your contract.  Without a profile image, it won't properly show up in the browser.

### Add / Edit Any Metadata

baseURI + Song metadata path = songURI

You can add/edit metadata files to any rarity of a song after it's been created. &#x20;

You can edit multiple rarities of metadata in one transaction.  You can edit multiple songs and multiple rarities in one transaction.  You can fix mistakes in the token URIs, or enhance the amount of rarities.

## Save Gas

If you enter the songURI for each token manually, then you would be entering in a new url for each rarity of each song.  If you use Arweave, that means a new tx\_id for each file, which is 43 characters long.  If you want to update something, you need to change everything one piece at a time.&#x20;

If you use a manifest, then each songURI is using a path based on the manifest, you can set the path and use the same one across versions, meaning you never need to change the path for each track and can still update the entire collection in one change. The 43 character paths are no longer a thing, they become a couple characters long. This saves so much gas. It really makes a huge difference in situations when every gas optimization counts. 43 characters becomes 1+ characters.
