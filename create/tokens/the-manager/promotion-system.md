# Promotion System

Promotions let you create token gated mints, free claims, discounts, rare mints, and anything else you can think of.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-19 at 3.28.39 AM.png" alt=""><figcaption></figcaption></figure>

## Promos Tab

In the Promos tab you can see all the active promotions for your contract.  You can see the requirements and reward for every promo.

### Set Promo

You can set a promotion with the "Set Promo" button, which opens up a bunch of fields to enter. For a contract wide promotion, you need to enter in 4 things.  For a specific promo you need to enter in 6 things.  A regular contract wide promo is compatible with all ERC-721 tokens.  Specific promotions are only available to ERC-721J tokens because they require a Song ID and Rarity.

A contract wide promo needs:

* Contract Address - The address where the promo requirement is from.  This contract address needs to be an ERC-721 standard contract.
* Price Multiplier Out - The cost to mint the promo, relative to the normal mint price. It's up to the artist to make promotions discounted, free, or above normal. Defaults to 0%, for free. 100 means regular mint price.
* Song ID Out - The Song ID of the reward. If Song ID Out is set to 0 it will reward the most recently created song.  So the promo could reward different songs over time if set to 0.
* Song Rarity Out - The Rarity of the reward. Has to be 2 or above. Setting Rarity Out to 0 will deactivate the promo.

A specific promo needs the additional:

* Song ID In - The Song ID required for a promo to be eligible.  If the Song ID is set to 0 that means any song from the Contract Address is able to mint.
* Generation In - The Generation required for a promo to be eligible.  If the generation is set to 0 that means any rarity from that Contract Address is able to mint.

### Promo Info

With this button you can look up any promo by the requirements and see what it rewards.&#x20;

### Token Check

With this button you can look up any token on any contract and see if it's claimed it's promos.

### Promo Viewer

The visual promo viewer in The Manager Page does a good job showing you the inputs and outputs of each promotion.  There is a drop down, search, and +/- buttons to flip through all the active promos. The "Promo Info" button is still there, but it's much easier to see it all visually with the promo viewer.

## How Promos Work

If you have a token in your wallet that matches a promotion requirement, then you are eligible to mint that promotion.  Tokens are only able to claim 1 regular promotion and 1 specific promotion per contract. A specific promotion is a promo that uses the extra rules only available to 721J tokens (rarity and song ids). Normal ERC-721 tokens will only be able to claim one regular promotion. Only 721J tokens will be able to claim 2 promos.
