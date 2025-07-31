# Minting Pages

You can create infinite amounts of minting pages for one or all collections. Anything your imagination can come up with you can build it.



## Prompts

Use these prompts to get started with building your own minting page.&#x20;

Always include the [721J ABI](../smart-contracts/the-code/abis.md) with these prompts.

Simple minting page:

{% code overflow="wrap" %}
```
I'm trying to make a website to interact with this smart contract I made. Here is the ABI: [add the ABI file here]

The contract address is [insert contract address (example 0xced6665f2f4568a4321892c52d894121a94eae36)] I want to use the tokenOfPublicByIndex function to find the token ids of all the public tokens and show that list of token ids on this new page.

Then I would like to use these token ids and look them up with the tokenURI function to get the url of the metadata for each token. Then I want to download the metadata JSON and find the image in the "image" field in the JSON that is downloaded. the audio file is in the "animation_url" field. And there's other fields too to display the tracks.

I would like to also have a button that uses the mintCopy function for each token that shows up in the list.

Show each track's information organized neatly with clean ui. 
```
{% endcode %}

More mint page prompts coming.

***

## Websim

You can use websim to help generate infinite minting pages of any asthetic you can think of.

### Examples

#### Basic Clean Start

Use this as a clean basic starting point to experiment with generative minting pages.&#x20;

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/3" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-30 at 11.48.49 PM.png" alt=""><figcaption></figcaption></figure>

***

#### Windows 95 Style

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer/13" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-31 at 12.14.22 AM.png" alt=""><figcaption></figcaption></figure>

***

#### The Matrix Style

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/41" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-31 at 1.37.22 AM.png" alt=""><figcaption></figcaption></figure>

***

#### 3D Gallery With ThreeJS

A basic ThreeJS art gallery.  The tokens available to mint show up on the walls of the art gallery, you can walk around, click on the tracks to listen to them, and click the mint button below each piece of art to mint a copy.&#x20;

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/36" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-31 at 1.39.11 AM.png" alt=""><figcaption></figcaption></figure>

***

#### Comic Book Style

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/44" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-31 at 2.17.33 AM.png" alt=""><figcaption></figcaption></figure>

***

#### Underground Vibes

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/4" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-30 at 10.53.08 PM.png" alt=""><figcaption></figcaption></figure>

***

#### Sleek Asthetics

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/17" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-30 at 11.51.22 PM.png" alt=""><figcaption></figcaption></figure>

***

## Just The Beginning

This is an example of what you can currently do with a few prompts.  They can be improved by including information about the supply of each song, the name of the collection, grabbing the contract metadata, etc. So much more to explore related to automated UIs for minting pages.&#x20;
