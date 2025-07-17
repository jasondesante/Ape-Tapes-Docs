# Noteworthy Traits

This is just a selection of all the traits in the Required and Optional tabs in The Song Metadata Maker.

### Resized Images

Resized images are important because sometimes the main image is giant, and the act of downloading and resizing it can be a lot more difficult than simply seeing that there is an image\_small or image\_thumb included and grab that directly.  Including resized images is such an important thing. &#x20;

It's the courteous thing to do in web3 is to think for the dapp ahead of you. That is a core value of this project.

### License

Similar to adding a license to the files themselves on Arweave, adding a license to the metadata file puts a license on the token, which is a collection of files that each have their own separate licenses.  It's like a license sandwich or something, licenseception. &#x20;

You could put different licenses on different rarities of tokens and then allow for all sorts of creative applications of the token.

## Audio

The audio metadata traits are separated into lossless and lossy categories.  That old "standard" field is "animation\_url".  This is where you will normally see the metadata for the audio on NFTs.  This is problematic because it's also suggested to put all sorts of stuff there, so you never really know if it's an audio file if it's in "animation\_url".  It's a possibility, but it's not the way you'd want to do things in the future.\
\
For audio you should still put it in "animation\_url" because who knows whether or not the marketplace or dapp or whatever will look for the better traits, just use "animation\_url" until the overall crypto community decides or whatever.

The actual traits you should care about for music are to use "audio\_url" and or "lossless\_audio" for the high quality uncompressed audio, and use  "mp3\_url" and or "lossy\_audio" for the lossy mp3 quality audio. I think those are more understandable, though it isn't clear which is the winner.  "audio\_url" and "mp3\_url" or "lossless\_audio" and "lossy\_audio".  My vote would be lossless\_audio and lossy\_audio because the pair makes the most sense.

Either way there are 5 fields in the metadata for audio.  The lossless audio is in 3 of those spots, and the lossy audio is in the other 2.  Hopefully one day we decide and reduce the 5 down to 2.

### Bit Depth / Sample Rate / Audio Quality

In the traits there's the bit\_depth and sample\_rate fields which each keep track of their respective values.  In the Attributes, there is something called Audio Quality which is the combination of the two traits.  Laid out as "sample rate/bit depth".  So an example of Audio Quality would be 44.1/16, or 96/24.

### Duration

This number is the length (in seconds) of the track.  If it's 1 minute and 9 seconds long you would enter 69.  Duration is very important because the player can then see the length of the track without having to download it.  This is good when you are looking at a large list of tracks, you don't want to have to download every audio file just to see how long it is. You want to be able to see the duration of each track quickly.

### ISRC

When you include an ISRC code in the metadata, it also gets added as an on-chain tag to the audio file on Arweave, forever marking the file with its ISRC code. This means every time your file is accessed, the ISRC is visible and verifiable, making The Contract Wizard's metadata maker big label friendly while ensuring permanent provenance for your music.

## Optional Metadata

### Genre / Tags

The genre and tags are important because curation is important for tracks and playlists. &#x20;

If a song doesn't include this metadata, then the track won't be curated as well. It will lead to cooler things if we properly tag stuff to begin with.

### Lyrics

Including the lyrics in the metadata lets them show up when playing the song, which is always a nice option.  Everyone likes the option of being able to view the lyrics while listening. Adding lyrics allows the player to show the lyrics to the listener.



## More Files

### Images

The images array is a cool trait to have because what if you want to include 20 images or something, like a large amount of liner notes and stuff?  I used to love that stuff when an album would have really cool notes, or a cd having a really good booklet.  This stuff matters.  You have the option to expand and do whatever you want with an endless list of images here. &#x20;

### Video

A video is a cool thing to include in your token.  It will show up in the player with an extra video icon you can click, enhancing the listening and viewing experience.

### Visualizer

The visualizer in this context is a video that plays the song.  Also known as a lyric video or visualizer video.  It's not exactly a music video, but it also isn't just a static image in a video playing the music.  It's something in between.  If you have such content it can go here. &#x20;

### Midi

Midi files are awesome.  Who doesn't like midi files?  If you're like me you probably have a folder of midi files of a bunch of your favorite songs.

## Make The Metaverse Real

### VRM

A VRM stands for Virtual Reality Modeling and is an easy to use format for 3d characters.  If you include a VRM in your metadata, holders will have an avatar that represents the track in virtual worlds.

You can also add your VRM to the music visualizer and watch your VRM dance with all the wizards.&#x20;

### Merch

You can attach a 3d file of a piece of digital merch that could be worn by your character in various games.

This could be a normal shirt or hat with just the design being unique, or it could be entirely unique fashion.  The possibilities are endless.  You really could do anything with digital merch that's intended for an avatar to wear.  You could even do something like socks here.  As long as it's built with some standardized characters in mind, there's a good chance that it will work.

### Step Mania

[Step Mania](https://www.stepmania.com/), and [Project OutFox](https://projectoutfox.com/), is a free cross platform (Linux, Mac, and PC) rhythm game engine that started as a fan version of Dance Dance Revolution.  You can make Step Mania charts for your songs.  Who wouldn't want to see Step Mania charts be tokenized like this, it could encourage more people to make Step Mania charts by showing people this is something they want.

### Clone Hero

[Clone Hero](https://clonehero.net/) is a free cross platform (Linux, Mac, PC, and Android) rhythm game that is similar to Guitar Hero and Rock Band by Harmonix.  You can make your own Clone Hero charts.  You can play Clone Hero with a guitar controller, midi drum kit and more. This just like Step Mania is something that we should all aspire towards.  I would love to see tokenized Clone Hero charts.  This is how we make the metaverse real by fixing the problems of old dlc.
