# Choosing An Image

Every playlist needs a good picture.  There are 4 options you can choose from when adding a playlist image:

* Pick an image
* Custom URL
* Generate Collage
* Upload Image

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-13 at 12.15.34 AM.png" alt=""><figcaption><p>The 4 main options when picking a playlist image</p></figcaption></figure>

### Pick An Image

Choosing Pick An Image gives you a few sets of images to choose from to pick a playlist image.  Those collections are:

* Ape Tapes - Apes as tapes by [Kupeh](https://twitter.com/kupeh_rod).
* Smol Tapes - Wizard tapes by [WizardSmol](https://twitter.com/wizardsmol).
* AI Music stores - A collection of music store images I generated with Midjourney

### Custom URL

You can enter any url that's already on the internet.  If it's an image it will show up and you can choose it.

Once a URL is set, two optional fields appear for **Small** (500px) and **Thumb** (50px) resized variants of the same artwork. If you have resized versions already on Arweave, paste their URLs in.

The **Select from Library** button opens the file picker with image grouping enabled — the same group-of-3 selection the Metadata Maker uses. If your artwork was uploaded with its resized pair (`-image_small` / `-image_thumb` files), pick the grouped trio and all three fields fill in at once. Picking a single image fills only the main URL and leaves the variant fields for you.

### Generate Collage

You can generate a clean or dirty collage that is made up of the artwork for the various songs in the playlist. The more tracks the more images.  Once a collage is generated it's uploaded to Arweave, and then set.&#x20;

![](<../../.gitbook/assets/Screenshot 2025-07-13 at 12.18.11 AM.png>)

A clean collage looks like all the artwork is neatly placed on a grid. Example below:

![](../../.gitbook/assets/2f084fc1-914b-4d54-ac2a-8ff3bbcfd949.jpeg)

A dirty collage looks like all the artwork is scattered on top of each other. Example below:

![](../../.gitbook/assets/dcd383e5-9565-4d00-9d95-5a774aaf532b.jpeg)

### Upload Image

This module lets you select any image on your computer and add that to be the playlist image.  When you add a file, it is uploaded to Arweave, and then set as the playlist image.

### Resized Variants (image_small / image_thumb)

Covers made with **Upload Image** or **Generate Collage** automatically get two resized variants uploaded alongside the main file: a 500px **small** and a 50px **thumb**. These land in the playlist's metadata as `image_small` and `image_thumb`, next to the full-size `image`.

Players that display playlist covers check `image_small` first and fall back to `image` — the smaller file loads faster on grids and mobile connections, and it gives third-party builders a light-weight cover out of the box. Swapping a cover for a preset image clears the old variants automatically, so the metadata never points at artwork you're no longer using.
