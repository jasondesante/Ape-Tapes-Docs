# Song Metadata

The Song Metadata Maker gathers the pictures for every rarity, audio file and all the information about the song.

### Automatic IPFS Links

The IPFS link shows up when you add any file.  You'll have the option later to upload to Arweave.

### tokenURI Function

Using the tokenURI or songURI functions on your smart contract will show you the song metadata.  It's set with the setSongURI function, or when an original is created. &#x20;

## Input Fields

### Required

The required fields in the Song Metadata Maker are: &#x20;

* Title
* Artist
* Song (Lossless)
* Image

### Optional

The other fields are optional for the Song URI.  Some optional fields for song metadata include:

* Album
* Track Number
* Collaborating Artists
* Artist Image
* Album Image
* ISRC
* UPC
* Lyrics
* Genres
* Tags
* Description
* Song (Lossy, Mp3)
* Video
* Visualizer
* Clone Hero Charts
* Step Mania Charts
* VRM (Avatar)
* Merch (3D Model)
* Midi

Additional categories of metadata that unlock new functionality are:

* Attributes
* Credits
* Stems
* Mixes

### Stems

Stems are a form of multi track.  You can include stems in the metadata which will give holders more content to remix with, as well as the ability to listen using a stem player.

### Mixes

Alternate mixes are another way to enhance the listening experience, similar to stems.  You can include as many alternate mixes as you can imagine.  You can even attach conditions to any mix which creates the possibility of a programmable experience to every song.  You can be as wild or subtle as you want with this powerful tool.  Think about Nintendo, Animal Crossing, Mario, the way the arrangements and mixes would change.  This is possible now with programmable mixes.





#### Lyrics

Adding lyrics allows the player to show the lyrics to the listener.

#### Video

Including a video with the song will make a video icon appear in the player.  Clicking on the video icon opens a video player.  Music videos are viewable right in the player next to everything else. &#x20;

#### ISRC

If you add the ISRC to the metadata, the ISRC will also get added to the audio file as an on chain tag on Arweave.  This is really cool to tag the file with the ISRC on Arweave because every time your file is read, you will be able to see the ISRC code related to the file.

#### VRMs

You can attach a VRM to the metadata which will let holders have an avatar that represents the song to use in metaverses.  You can also add your VRM to the music visualizer and watch your VRM dance with all the wizards.&#x20;

#### Digital Merch

Similar to VRM, you can attach a 3d file of a piece of digital merch that could be worn by your character in various games.





## Creating Metadata

Making metadata is easy.  First thing is to gather your files.  Fill out the required fields.  Fill out as many optional fields as you want.  Now you're ready for the next step.

## Saving

Click save when you're finished adding files.  [Add a license](add-license.md), upload to Arweave, or skip and use IPFS.

It's highly recommended to upload your files to Arweave. To do that you'll need to have a balance on [Irys](./#irys) larger than the price. You can deposit to the [Irys](./#irys) contract with the button in the details.

Once you sign, the files are uploaded.  The IPFS links are replaced with the new Arweave links, and the metadata files are created. &#x20;

### Downloading

You will then see a button to download every rarity in a zip, as well as the IPFS links to the finished metadata.

There's also the option to download the raw metadata.  The raw file is there to recover as a save state when updating the metadata later.  One reason the raw is best for updating is the rarities are in the one file.



Now you're done creating the song metadata!
