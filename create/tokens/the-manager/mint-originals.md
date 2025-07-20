# Mint Originals

You can create new originals on The Manager page. This is the most important functionality on the page.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-19 at 12.05.40 AM.png" alt=""><figcaption></figcaption></figure>

## Before Minting

Minting the original token is the last step. Previous steps include uploading the files, creating every metadata file and uploading a manifest. Are you ready?

### Requirements

You'll be required to set the total supply of copies and the metadata link for each rarity.  An optional parameter is split address, which unlocks royalty splits.

## Creating A New Master Token

If you used The Manifest Maker to create your baseURI, you should see a drop down menu to visually select the metadata for the song.  If not you'll only have input mode as an option. &#x20;

The choice of 1-3 rarities is meant to provide an option and not force someone to do the default 3 metadata variations.

***

## Input Modes

### List Mode

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-19 at 12.05.53 AM.png" alt=""><figcaption></figcaption></figure>

The list mode lets you visually see the picture for each piece of metadata, you can also search to filter if your manifest is a large list.  This makes selecting the metadata a lot easier than remembering the paths for each rarity. This is a huge improvement.

***

### Input Mode

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-19 at 12.06.01 AM.png" alt=""><figcaption></figcaption></figure>

Input Mode is the manual way of entering in the data, writing in the songURI on your own.  Make sure you don't make any mistakes! This isn't complicated, but it's easier to make mistakes and takes longer to do.

Input mode does check the file path and lets you know if you wrote something that doesn't lead to a metadata file. You'll see the baseURI written up top so you can figure out the finished urls too.

***

## Parameters

### Song URI

The Song URI is the path to the metadata file.  The Base URI + Song URI = the finished link to the metadata.

### Total Supply

The max supply is the total amount of copies of a song that can exist.  Every song starts as one original, and every copy adds one to the supply. Rarity of copies is a thing so you can still have scarcity with a large supply.  You can be creative with how you think about rarities and supply.

### Splits

Enter a split contract address and it unlocks new functionality for on chain royalty splits.  When an address is entered as the split address, all the eth and tokens that song receives will go to that address rather than the owner of the contract.  This allows the artist to have customized royalty splits for every song. &#x20;

With split contracts you can give royalties to your collaborators, as well as do cool things like tokenize the royalties.  So the royalties are going to owners of tokens instead of a set wallet address.  This makes royalties a tradeable thing if you choose to do that.

It is highly recommended to [use 0xSplits](https://app.splits.org/) for their high quality split contracts. [Read more](https://docs.splits.org/)

***

## Clicking Mint

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-19 at 12.31.07 AM.png" alt=""><figcaption></figcaption></figure>

Once you're comfortable, mint the original and The Contract Wizard will congratulate you.  The Manager page should have an updated total of originals and shortly after your wallet should refresh.

With a new song in your contract, you can now mint copies of it, stake it, share it, and add it to a playlist.

## Help

If you need help you can toggle the hat helper switch, check this page, or reach out on [X](https://twitter.com/jasondesante).&#x20;

