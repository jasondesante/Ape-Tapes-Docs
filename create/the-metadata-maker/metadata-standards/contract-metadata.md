---
description: 721J Metadata Standards
---

# Contract Metadata

## Contract Metadata

Every contract has a function for a contractURI, where metadata for the contract lives. &#x20;

You can set a profile image, banner image, and more to be grabbed by any dapp.  Compare this to a contract like ape coin, which doesn't even have the ape coin logo available anywhere from the contract! That contract isn't special, it's really a thing no one does, but it could be a thing everyone does because it makes sense and isn't difficult. It also gives the owner of the contract more stuff to be creative with, when they have their spot in their contract to put a contractURI. &#x20;

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

### Images

The images array is cool because you might want to provide a bunch of pictures for your contract metadata to have a lot of fun or tell a larger story.  There's many reasons you might want to do a little bit of world building.

### Resized Images

Resized images are important because you sometimes want a tiny thumbnail or an optimized small version of the image, rather than the original or uncompressed version of the image.  Having the different image sizes improves performance tremendously.

It's thinking about the dapp ahead of you.
