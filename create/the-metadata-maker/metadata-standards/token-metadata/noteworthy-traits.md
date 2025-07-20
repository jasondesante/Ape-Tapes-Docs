# Noteworthy Traits

This is just a selection of all the traits in the Required and Optional tabs in The Song Metadata Maker.

### Resized Images

Resized images are important because sometimes the main image is giant, and you only need a thumbnail or small version of the image.  The act of downloading and resizing it can be a lot more difficult than grabbing the image\_small or image\_thumb field.

It's the courteous thing to do in web3 is to think for the dapp ahead of you. That is a core value of this project.

### License

Similar to adding a license to the files themselves on Arweave, adding a license to the metadata file puts a license on the token. Token licenses are a level above the files. &#x20;

You could put different licenses on different rarities of tokens and then allow for all sorts of creative applications of the token.

## Audio

The audio metadata traits are separated into lossless and lossy categories.  The "standard" field is "animation\_url".  This is where you'll normally see the metadata for the audio on NFTs.  This is problematic because it's also suggested to put other stuff there, so you never really know if it's an audio file when it's got "animation\_url".  It's not the way you'd want to do things in the future, because having something in "animation\_url" doesn't guarantee it's audio, it could be a video or something else.\
\
For audio you should still put it in "animation\_url" because who knows whether or not the marketplace or dapp or whatever will look for the better traits, just use "animation\_url" until the overall crypto community decides.

The actual traits you should care about for music are "audio\_url" and or "lossless\_audio" for the high quality uncompressed audio, and "mp3\_url" and or "lossy\_audio" for the streaming quality audio. I think those are more understandable, though it isn't clear which is the winner.  "audio\_url" and "mp3\_url" or "lossless\_audio" and "lossy\_audio".  My vote would be lossless\_audio and lossy\_audio because the pair makes the most sense.

Either way there are 5 fields in the metadata template for audio.  The lossless audio is in 3 of those spots, and the lossy audio is in the other 2.  Hopefully one day we decide and reduce the 5 down to 2.

### Bit Depth / Sample Rate / Audio Quality

In the metadata there's the bit\_depth and sample\_rate fields which each keep track of their respective values.  In the Attributes, there is something called Audio Quality which is the combination of the two traits.  Laid out as "sample rate/bit depth".  So an example of the Audio Quality attribute would be 44.1/16, or 96/24.

### Duration

This number is the length (in seconds) of the track.  If it's 1 minute and 9 seconds long you would enter 69.  Duration is very important because the player can then see the length of the track without having to download it.  This is good when you're looking at a large list of tracks. You don't want to have to download every file just to see how long each track in the playlist is. You want to be able to know the duration of each track from the metadata.

### ISRC

When you include an ISRC code in the metadata, it also gets added as an on-chain tag to the audio file on Arweave, forever marking the file with its ISRC code. This means every time your file is accessed, the ISRC is visible and verifiable, making The Contract Wizard's metadata maker big label friendly while ensuring permanent provenance for your music.

## Optional Metadata

### Genre / Tags

The genre and tags are important because they are core to curation. Curation is important for both tracks and playlists, because it's how quality will rise.

If a song doesn't include this metadata, then the track won't be curated as well. Tagging stuff is an essential part of the uploading routine.

### Lyrics

Including the lyrics in the metadata lets them show when playing.  Everyone likes the option to view the lyrics while listening. Adding lyrics to the metadata allows all players to show the lyrics to the listener if they want.

## More Files

### Images

The images array is a cool trait to have because what if you want to include 20 images or something, or a large amount of liner notes?  I love that stuff when an album has really cool notes and pictures.  This stuff matters, it might sound corny but it's world building and that's important.  You have the option to expand and do whatever you want with an endless list of images here. &#x20;

### Video

A video is a cool thing to include in your token.  It'll show up in the player with an extra video icon you can click, enhancing the listening and viewing experience.

### Visualizer

The visualizer in this context is a video that plays the song.  Also known as a lyric video or visualizer video.  It's not exactly a music video, but it also isn't just a static image in a video playing the music.  It's something in between.  If you have such content it can go here. &#x20;

### Midi

Midi files are awesome.  Who doesn't like midi files? Including the midi charts of the music is some next level stuff.

## Make The Metaverse Real

### VRM

A VRM is a file type for 3d characters that stands for "Virtual Reality Modeling" file.  If you include a VRM in your metadata, holders will have an avatar they can use in virtual worlds.

You can also add your VRM to the music [visualizer](../../../../consume/universal-music-player/visualizer/) and watch your VRM dance with all the wizards.&#x20;

### Merch

You can attach a 3d file of a piece of digital merch that could be worn by a character in various games.

This could be a normal shirt or hat with just the logo being unique, or it could be entirely unique models.  The possibilities are endless.  You really could do anything with digital merch that's intended for an avatar to wear.  You could even do something like socks here.  As long as it's built with some standardized characters in mind, there's a good chance that it will work.

### Step Mania

[Step Mania](https://www.stepmania.com/), and now [Project OutFox](https://projectoutfox.com/), is a free cross platform (Linux, Mac, and PC) rhythm game engine that started as a fan version of Dance Dance Revolution.  You can make Step Mania charts for your songs.  Who wouldn't want to see rhythm game charts be tokenized like this, it could encourage more artists to make charts and encourage growth in those open rhythm games. Tokens seems like a great way for such open free projects to find a way to monetize while collaborating with artists.

### Clone Hero

[Clone Hero](https://clonehero.net/) is a free cross platform (Linux, Mac, PC, and Android) rhythm game that is similar to Guitar Hero and Rock Band by Harmonix.  You can make your own Clone Hero charts.  You can play Clone Hero with a guitar controller, midi drum kit and more. This just like Step Mania is something that we should all aspire towards.  I would love to see tokenized Clone Hero charts.  A good step to making the metaverse real is by fixing the problems of old dlc.
