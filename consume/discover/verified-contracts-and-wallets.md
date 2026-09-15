# Verified Contracts & Wallets

You'll see a checkmark next to contract names and wallet names around the app. It means one thing: that address has an ENS name attached to it.

The checkmark isn't handed out by a central authority. It comes straight from ENS, and anyone can get it by setting things up right.

## How Verification Works

ApeTapes checks the ENS binding in both directions: the address's reverse record names the ENS, and the ENS resolves forward to that same address. A self-claimed reverse record that doesn't resolve back doesn't count.

The lookup always runs on Ethereum mainnet, since that's where ENS lives. A contract favorited on Polygon or another chain won't show a checkmark, even if the same contract is verified on mainnet.

## The Matching Rule

For contracts there are two levels:

**Name + ENS match.** The contract's collection name matches its ENS name. The collection name gets displayed with the checkmark. This is the strong one, and the one you want as an artist.

**ENS only.** The address has an ENS but the name doesn't match the collection name. It still gets a checkmark, but the ENS name is displayed instead of the collection name.

The match ignores things that don't change identity:

* Capitalization: `CosmoDoris` = `cosmodoris`
* The `.eth` suffix
* Spaces: `Cosmo Doris` = `CosmoDoris`
* Version suffixes: `Night Signals v3` = `Night Signals`

So a contract named "Night Signals v3" matches `nightsignals.eth`, and "My Label V2" matches `mylabel.eth`.

## For Wallets

A wallet gets the checkmark when its primary name is set, meaning the wallet's reverse record points at an ENS. Hovering the checkmark explains exactly what was found.

## How To Get Verified

1. Name your contract something you can register as an ENS. This is the step people skip and regret.
2. Register the ENS.
3. Point the ENS at the address. For a wallet, that means setting the wallet's primary name (reverse record). For a contract, the binding has to work both ways: the contract's reverse record names the ENS, and the ENS resolves to the contract address.
4. Open the Contract Manager and use Verify ENS to check it, then Sync to pull the record onto the server.

That's it. The Wizard's Library, the Featured page, and the Library page all pick it up from there.

## Where You See It

* Library followed collections (contracts and wallets)
* The player page, next to the collection/wallet title (shown when the name comes from a resolved ENS)
* The Wizard's Library rail on the Featured page
* The Contract Manager (the ENS pill and the Current ENS row)
* Search — type an ENS with or without the `.eth` and it resolves (see [Search](../search.md))

## Good To Know

Verification is read live in most places, but favorites store the ENS from the moment you favorited. If an artist sets their ENS after you favorited them, unfavorite and re-favorite to refresh it. Contract owners can use the Sync button in the Manager to refresh the server copy anytime.
