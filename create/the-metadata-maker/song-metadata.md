# Song Metadata

The Song Metadata Maker gathers the audio file, pictures and everything else to create magic like you've never seen before.

There's a lot of possible fields when creating metadata for a track. The Song Metadata Maker is currently organized by tabs.

## Required

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-16 at 11.45.53 PM.png" alt=""><figcaption></figcaption></figure>

The required fields in the Song Metadata Maker are: &#x20;

* Title
* Artist
* Audio
* Image

The "Required" tab also contains some optional fields such as:

* Album
* Track Number
* Collaborating Artists
* [ISRC](metadata-standards/token-metadata/noteworthy-traits.md#isrc)

## Optional

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-16 at 11.48.57 PM.png" alt=""><figcaption><p>Open each category to see what's inside!</p></figcaption></figure>

The optional tab is broken down into 3 main categories: Album/Project, Metadata, and Files. &#x20;

Album contains all the fields related to the album, like album art.  The "Metadata" named section contains all the extra general metadata for the track, like genre, tags, description, year, and much more. The Files section contains all the extra files you would upload like video, mp3, extra images, and more.

These other fields are all optional for the Song URI.  Some notable optional fields include:

#### Album/Project

* Album Image
* UPC

#### Metadata

* [Lyrics](song-metadata.md#lyrics)
* [Genres](metadata-standards/token-metadata/noteworthy-traits.md#genre-tags)
* [Tags](metadata-standards/token-metadata/noteworthy-traits.md#genre-tags)
* Description

#### Files

* Artist Image
* [Song (Lossy, Mp3)](metadata-standards/token-metadata/noteworthy-traits.md#audio)
* [Video](metadata-standards/token-metadata/noteworthy-traits.md#video)
* [Visualizer](metadata-standards/token-metadata/noteworthy-traits.md#visualizer)
* [Clone Hero Charts](metadata-standards/token-metadata/noteworthy-traits.md#clone-hero)
* [Step Mania Charts](metadata-standards/token-metadata/noteworthy-traits.md#step-mania)
* [VRM (Avatar)](metadata-standards/token-metadata/noteworthy-traits.md#vrm)
* [Merch (3D Model)](metadata-standards/token-metadata/noteworthy-traits.md#merch)
* [Midi](metadata-standards/token-metadata/noteworthy-traits.md#midi)



## Extra

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-16 at 11.56.53 PM.png" alt=""><figcaption></figcaption></figure>

The Extra tab contains additional categories of metadata that unlock new functionality. These are:

* [Attributes](metadata-standards/token-metadata/grouped-traits.md#attributes)
* [Credits](metadata-standards/token-metadata/grouped-traits.md#credits)
* [Stems](metadata-standards/token-metadata/grouped-traits.md#stems)
* [Mixes](metadata-standards/token-metadata/grouped-traits.md#mixes)

### Metadata Functions

For contract owners, set the metadata with setSongURI function, or when an original is created.  &#x20;

View the metadata with the tokenURI or songURI functions on your smart contract. &#x20;

