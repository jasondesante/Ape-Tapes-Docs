---
description: 721J Metadata Standards
---

# Contract Metadata

## Contract Metadata

Every contract has a function for a contractURI, where metadata for the contract can go.  This lets you set a profile image, banner image, and any other images, which can be grabbed by any dapp.  Compare this to a contract like ape coin, which doesn't even have the ape coin logo available anywhere from the contract! &#x20;

Contract metadata is something that needs to be added to the standard for all ERC-20 and ERC-721 tokens, in my opinion.&#x20;

Please use this template below for inspiration when writing contract metadata.

{% embed url="https://github.com/jasondesante/721J-Token/blob/master/Metadata%20Templates/contract_uri_template_blank.json" %}

```
// Contract Metadata Template
{
    "name": "",
    "description": "",
    "platform": "Contract Wizard",
    "image": "",
    "images": [
        "",
        "",
        ""
    ],
    "image_still": "",
    "image_small": "",
    "image_large": "",
    "image_banner": "",
    "image_banner_still": "",
    "external_url": "",
    "external_link": "",
    "website": "",
    "opensea": "",
    "discord": "",
    "twitter": "",
    "spotify": "",
    "soundcloud": "",
    "bandcamp": "",
    "tidal": "",
    "instagram": "",
    "fee_recipient": "",
    "seller_fee_basis_points": ""
}
```

## Noteworthy Traits

### Description

The description of the collection is important because we are naturally curious.

### Social Media Links

There are a lot of options for social media links in the template, and you can add any amount more that aren't in the template.  It's meant to be customizable.  The social media platforms in the template are:

* X
* Spotify
* SoundCloud
* Bandcamp
* Tidal
* Instagram
* Discord
* OpenSea

### [Images](token-metadata.md#images)

More info [here.](token-metadata.md#images)

### [Resized Images](token-metadata.md#resized-images)

More info [here.](token-metadata.md#resized-images)
