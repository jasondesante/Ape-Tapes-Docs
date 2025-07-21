# How to Create an Original

Starting this tutorial assumes you have already completed creating and uploading all of your metadata files.  If not, check out [making-metadata-tutorials-2023](../old/making-metadata-tutorials-2023/ "mention") or the video tutorial.

## Contract Manager

To create an original 1/1:

1. Click "Create" on the sidebar

{% embed url="https://dv5nu56xnmqu26fohr5rivkcpijqlsu637ux3yl4sk6v4i6e2cmq.arweave.net/HXrad9drIU14rjx7FFVCehMFyp7f6X3hfJK9XiPE0Jk" %}

2. Click "Contract Manager" and load up the manager page
3. On the Contract Manager page, find the "Mint Master" button and click it

{% embed url="https://lncis2vsx5d72p4gworltz7igcvythdiwkie3dkhwy5777er3snq.arweave.net/W0SJarK_R_0_hrOiuefoMKuJnGiykE2NR7Y7__yR3Js" %}

4. You then have a choice for how many pieces of metadata to set.  Does your token have 1 piece of metadata that the original and copies share? Do you include another piece of metadata for generation 2? Or add 3 pieces of metadata (which I consider to be the right amount to start).
5. Enter in the Song URIs for each piece of metadata, and the total supply (maximum amount of copies) for the song.

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 1.22.44 AM.png" alt=""><figcaption></figcaption></figure>

6. Click Mint
7. Confirm in your wallet, wait
8. Celebrate!

## Song URI

A "Song URI" is another term for a link to the metadata.  URI 1, 2, and 3 correspond to setting generation 1, 2, and 3's metadata. Each URI goes to a different link of metadata that was created earlier, to distinguish each rarity for one song.

In the case of the 721J token, the metadata is made up of a "Base URI" + a "Song URI".  The Base is the beginning part, and the Song URI is combined with the base to make the full link.  The Base URI contains the part of the link that is repeated, for example "https://arweave.net/" or if you are using a manifest on Arweave "https://arweave.net/\*manifest tx\*/".

If you are not using a manifest on Arweave, you will have to enter the arweave tx as the Song URI for every piece of metadata.  If you are using a manifest, all you need to do is enter the name of the file for the Song URI.

## Total Supply

The total supply you set when creating an original is the maximum amount of copies you'd want to make for a song.  You can set it to as large or as small of a number you want, and you can also change it later.  If you change it later, an event will be emitted that will signal that a particular song has had it's total changed at some point, to help holders understand.

## Split Contracts

If you want to split all sales for a song on chain between collaborators, you might want to use a split contract to do that.  Splits are supported by the 721J v2 contract from the Contract Wizard.

With a split contract, you can manage all sorts of crazy splitting up of royalties on chain.  All you need to do is enter the split address when creating an original.

You can also have the flexibility to change the split address after creating an original.

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 1.23.45 AM.png" alt=""><figcaption></figcaption></figure>

## Video

{% embed url="https://youtu.be/wRmICbb2ZvQ" %}

## How To Make A Split Contract



Check out [#0xsplits](../../misc/external-links/#0xsplits "mention")

