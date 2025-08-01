# Minting Pages

**What if you could describe your dream minting page and watch AI build it for you?**

That's exactly what's happening here. Feed an AI the right prompts—complete with your contract's ABI for context—and watch it generate infinite variations of minting pages. Want yours to look like a retro arcade? A sleek Apple store? A cyberpunk terminal? Just ask.

The secret sauce is in the prompts. They're crafted to give AI everything it needs: your smart contract's interface, the specific functions to call, and how to display your tokens. Then you just describe the vibe you want, and use a custom minting page that actually works.

Every contract in The Wizard's Library shares the same smart contract interface, so any page you generate works for ALL collections. Build a Matrix-style minter? It'll work for every artist's contract. Create a comic book aesthetic? Same deal. This is the power of standardization meeting creative chaos.

**Break free from boring mint pages.** Why settle for the same sterile "Connect Wallet → Mint" experience when you can create something that makes people stop scrolling and say "I need to see what this is about"?

## Prompts

Use these prompts to get started with building your own minting page.&#x20;

Always include the [721J ABI](../smart-contracts/the-code/abis.md) with these prompts.

**Simple minting page:**

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

[Websim](https://websim.ai) turns your wildest aesthetic dreams into functional minting pages. Think of it as a design playground where "what if my mint page looked like..." becomes reality in minutes.

### Examples

**Basic Clean Start**\
Sometimes you need a solid foundation. Use this as your jumping-off point for more adventurous experiments.

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/3" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-30 at 11.48.49 PM.png" alt=""><figcaption></figcaption></figure>

***

**Windows 95 Style**\
Nostalgia meets NFTs.

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer/13" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-31 at 12.14.22 AM.png" alt=""><figcaption></figcaption></figure>

***

**The Matrix Style**\
Green cascading code, dramatic reveals. Your tokens have never felt more cyberpunk.

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/41" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-31 at 1.37.22 AM.png" alt=""><figcaption></figcaption></figure>

***

**3D Gallery With ThreeJS**\
Step into an actual art gallery where your tokens hang on virtual walls. Walk around, listen to tracks, and mint copies like you're collecting masterpieces in a museum. This isn't just a webpage—it's an experience.

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/36" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-31 at 1.39.11 AM.png" alt=""><figcaption></figcaption></figure>

***

**Comic Book Style**\
POW! BOOM! Your mints come alive with comic book energy. Every transaction feels like a superhero origin story.

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/44" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-31 at 2.17.33 AM.png" alt=""><figcaption></figcaption></figure>

***

**Underground Vibes**\
Raw, gritty, authentic. For when your music needs a minting experience that matches its underground energy.

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/4" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-30 at 10.53.08 PM.png" alt=""><figcaption></figcaption></figure>

***

**Sleek Aesthetics**\
Clean lines, smooth animations, premium feel. When you want your minting page to feel as polished as your music.

{% embed url="https://websim.com/@dawnshadow37236020/public-tokens-viewer-2/17" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-30 at 11.51.22 PM.png" alt=""><figcaption></figcaption></figure>

***

## This Is Just the Appetizer

What you're seeing here barely scratches the surface. Each example was generated with just a few prompts, but they can evolve into something magnificent. Add real-time supply tracking, collection metadata integration, social features—the sky's the limit.

The real magic happens when you realize these aren't just pretty interfaces. They're functional, working demonstrations of what's possible when creativity meets smart contract standardization. Your minting page becomes part of the art itself.

**Ready to build something nobody's seen before?**
