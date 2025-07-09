---
description: 721J Metadata Standards
---

# Token Metadata

## Token Metadata

Check the version of the template on GitHub with examples to see what is required for each field of metadata.  Please use this template below for inspiration when writing metadata for a token.

{% embed url="https://github.com/jasondesante/721J-Token/blob/master/Metadata%20Templates/token_uri_template_blank.json" %}

{% code fullWidth="false" %}
```
// Token Metadata Template
{
    "version": "",
    "name": "",
    "title": "",
    "duration": 7,
    "artist": "",
    "artists": [
        {
            "name": "",
            "type": ""
        },
        {
            "name": "",
            "type": ""
        }
    ],
    "album": "",
    "track_number": 7,
    "genre": [
        "",
        ""
    ],
    "year": 7,
    "mime_type": "",
    "bit_depth": 16,
    "sample_rate": 44.1,
    "tags": [
        "",
        "",
        ""
    ],
    "key": "",
    "bpm": 7,
    "description": "",
    "description_artist": "",
    "license": "",
    "location_created": "",
    "isrc": "",
    "project": {
        "title": "",
        "artwork": {
            "mime_type": "",
            "uri": "",
            "thumb": "",
            "small": "",
            "large": ""
        },
        "artist": "",
        "description": "",
        "type": "",
        "original_release_date": "",
        "record_label": "",
        "publisher": "",
        "upc": ""
    },
    "lyrics": {
        "text": ""
    },
    "visualizer": {
        "mime_type": "",
        "uri": ""
    },
    "video": {
        "mime_type": "",
        "uri": ""
    },
    "artwork": {
        "mime_type": "",
        "uri": "",
        "thumb": "",
        "small": "",
        "large": ""
    },
    "external_url": "",
    "image": "",
    "image_thumb": "",
    "image_small": "",
    "image_large": "",
    "image_album": "",
    "image_album_thumb": "",
    "image_album_small": "",
    "image_album_large": "",
    "image_artist": "",
    "image_artist_thumb": "",
    "image_artist_small": "",
    "images": [
        "",
        "",
        "",
        "",
        ""
    ],
    "original_release_date": "",
    "record_label": "",
    "publisher": "",
    "rarity": "",
    "attributes": [
        {
            "trait_type": "Rarity",
            "value": ""
        },
        {
            "trait_type": "Title",
            "value": ""
        },
        {
            "trait_type": "Artist",
            "value": ""
        },
        {
            "trait_type": "Album",
            "value": ""
        },
        {
            "trait_type": "Track Number",
            "value": ""
        },
        {
            "trait_type": "Audio Quality",
            "value": ""
        },
        {
            "trait_type": "Year",
            "value": ""
        },
        {
            "trait_type": "Cover Artist",
            "value": ""
        }
    ],
    "mp3_url": "",
    "lossy_audio": "",
    "audio_url": "",
    "lossless_audio": "",
    "animation_url": "",
    "vrm": "",
    "merch": {
        "mime_type": "",
        "type": "",
        "uri": ""
    },
    "midi": "",
    "step_mania": "",
    "clone_hero": "",
    "credits": [
        {
            "name": "",
            "credit": ""
        },
        {
            "name": "",
            "credit": ""
        },
    ],
    "stems": [
        {
            "name": "",
            "mime_type": "",
            "uri": ""
        },
        {
            "name": "",
            "mime_type": "",
            "uri": ""
        },
    ],
    "mixes": [
        {
            "name": "",
            "mime_type": "",
            "uri": "",
            "conditions": [
                {
                    "type": "",
                    "value": ""
                },
                {
                    "type": "",
                    "value": ""
                },
            ]
        },
        {
            "name": "",
            "mime_type": "",
            "uri": "",
            "conditions": [
                {
                    "type": "",
                    "value": ""
                }
            ]
        },
    ]
}

```
{% endcode %}





## Trait Groups

### Attributes

Attributes is an array of traits that show up when you view an NFT on a marketplace site like Opensea, Magic Eden, Blur, etc. Those traits that normally show up are the attributes.

### Credits

Credits is an array of traits that describe the individual credits for the token.  In here you can be as detailed as you want.

### Stems

Stems are a form of multi track, where each stem is an individual or group of tracks, combined form the song.  Providing stems unlocks remixing potential, stem player potential.  This is an important option to have in a music nft metadata standard.

### Mixes

Alternate mixes are a special feature that lets you provide any amount of extra mixes, and add any amount of conditions that can trigger that mix to play.  This lets you program all sorts of things only experienced in the best video games, as well as let you imagine new things that haven't been done before.  This is a very serious important feature, this is why we're here.

Some example conditions that have been built into [The Metadata Maker](../) are:

* Weight - set the number to weigh the mix's chance of being chosen when randomized.  For example if there are 3 mixes, with weights 1, 2, and 3. That adds up to 6 points across 3 mixes. The mix with weight 3 will occupy 3/6 total chances of being picked.  The mix with weight 1 will have a 1/6 chance.  The mix with weight 2 will have a 1/3 chance of being picked.  The mix with weight 3 will have a 1/2 chance of being picked.  Because the weights are all added up, and that's how you get your probability.
* Weather - set the weather to be able to play the mix
* Day - set the day of the week to be able to play the mix
* Start Time - set the start time of day to be able to play the mix.  Before the start time the mix is unplayable, starting at midnight, unless an End Time is also set.
* End Time - set the end time of day to be able to play the mix.  After the end time the mix is unplayable until the next day.  Resets at midnight unless a Start Time is also set.
* Minimum Plays - set the min number of plays to be on a song for this mix to be playable (can be 0 or higher).  This makes the mix unlocked after a certain amount of logged plays.
* Maximum Plays - set the max number of plays to be on a song for this mix to be playable (can be 1 or higher).  This makes the mix unplayable after a certain amount of logged plays.
* Every x Plays - set how many plays in between this mix having another chance to be played (can only be 2 or higher).  Once it's been played you have to wait a certain amount of logged plays until it's weights affect the mix choice.
* Altitude - will play at a certain altitude
* Favorite - will play if you favorite the song
* Birthday - will play on your birthday



## Noteworthy Traits

### Duration

This is a very important trait.  It's just a number, but it's a very important number.  This number is the length (in seconds) of the track.  If it's 1 minute and 9 seconds long you would enter 69.  Duration is very important because the player can then see the length of the track without having to download it.  This is good when you are looking at a large list of tracks, you don't want to have to download every audio file just to see how long it is so you can scroll up and down in the list.

### Images

The images array is a cool trait to have because what if you want to include 20 images or something, like a large amount of liner notes and stuff?  I used to love that stuff when an album would have really cool notes, or a cd having a really good booklet.  This stuff matters.  You have the option to expand and do whatever you want with an endless list of images here. &#x20;

### Resized Images

Resized images are important because sometimes the main image is giant, and the act of downloading and resizing it can be a lot more difficult than simply seeing that there is an image\_small or image\_thumb included and grab that directly.  Including resized images is such an important thing.  It's the courteous thing to do in web3 is to think for the dapp ahead of you, and try to make their lives easier.

### Video

A music video is a cool thing to include in your token.  It will show up in the player with an extra clickable video icon, enhancing the listening and viewing experience.

### Visualizer

The visualizer in this context is a video that plays the song.  Also known as a lyric video or visualizer video.  It's not exactly a music video, but it also isn't just a static image in a video playing the music.  It's something in between.  If you have such content it can go here. &#x20;

### Lyrics

Including the lyrics in the metadata lets them show up when playing the song, which is always a nice option.  Everyone likes the option of being able to view the lyrics while listening.

### Genre / Tags

The genre and tags are important because it's the only way playlists will be able to generate accurate genre and tags is by accumulating all the genres and tags from every song. &#x20;

If a song doesn't include this metadata, then the playlist can't be as accurate without having to rely on other analysis tools.  It's possible to run analysis software on the playlist afterwards, but I know it will lead to cooler things if we properly tag stuff to begin with.  If we tag the stuff once properly at the beginning that's a lot better than forcing every user to analyze and tag stuff on their end.

### Bit Depth / Sample Rate / Audio Quality

In the traits there is bit\_depth and sample\_rate which each keep track of their respective values.  In the Attributes, there is something called Audio Quality which is actually the combination of the two traits.  Laid out as /sample rate/bit depth.  So an example of Audio Quality would be 44.1/16, or 96/24.

### Audio

The audio metadata traits are separated into lossless and lossy categories, with another trait being the Opensea standard suggested field for music.  That old Opensea standard field is "animation\_url".  This is where you will normally see the metadata for the audio on NFTs.  This is problematic because it's also suggested to put all sorts of stuff there, so you never really know if it's an audio file if it's in "animation\_url".  It's a possibility, but it sucks, it's not the way you'd want to do things in the future.\
\
For audio you should still put it in "animation\_url" because who knows whether or not the marketplace or dapp or whatever will look for the better traits, just use "animation\_url" until the overall crypto community decides or whatever.

The actual traits you should care about for music are to use "audio\_url" and or "lossless\_audio" for the high quality uncompressed audio, and use  "mp3\_url" and or "lossy\_audio" for the lossy mp3 quality audio. I think those are more understandable, though it isn't clear which is the winner.  "audio\_url" and "mp3\_url" or "lossless\_audio" and "lossy\_audio".  My vote would be lossless\_audio and lossy\_audio because the pair makes the most sense.

Either way there are 5 fields in the metadata for audio.  The lossless audio is in 3 of those spots, and the lossy audio is in the other 2.  Hopefully one day we decide and reduce the 5 down to 2.

### Midi

Midi files are awesome.  Who doesn't like midi files?  If you're like me you probably have a folder of midi files of a bunch of your favorite songs.  Why not have a midi version right in the token that hooks up to a midi player?&#x20;

### ISRC

When you include an ISRC code in the metadata, it also gets added as a tag to the audio file on Arweave, which makes the ISRC code inescapable.  The file is forever marked on chain with the ISRC code.  That means The Contract Wizard's metadata maker is big label friendly.

### License

Similar to adding a license to the files themselves on Arweave, adding a license to the metadata file puts a license on the token, which is a collection of files that each have their own separate licenses.  It's like a license sandwich or something, licenseception.  You could put different licenses on different rarities of tokens and then allow for all sorts of creative applications of the token.  Remember the license on the token is different than the licenses on the files, and they can be as separate or combined as you choose.  You can use the distinction between file licenses and token licenses to do different things if you wish.

### VRM

A VRM stands for Virtual Reality Modeling and is an easy to use format for 3d characters.  If you include a VRM in your metadata, there are lots of programs that can read that from the token and let you control your character in these worlds.

### Merch

This could be a normal shirt or hat with just the design being unique, or it could be entirely unique fashion.  The possibilities are endless.  You really could do anything with digital merch that's intended for an avatar to wear.  You could even do something like socks here.  As long as it's compatible with Unreal Engine's standardized characters, there's a good chance that it will work.  That's how I'm thinking about it.&#x20;

### Step Mania

[Step Mania](https://www.stepmania.com/) is a free cross platform (Linux, Mac, and PC) rhythm game engine that started as a fan version of Dance Dance Revolution.  You can make Step Mania charts for your songs.  Who wouldn't want to see Step Mania charts be tokenized like this, it could encourage more people to make Step Mania charts by showing people this is something they want.

### Clone Hero

[Clone Hero](https://clonehero.net/) is a free cross platform (Linux, Mac, PC, and Android) rhythm game that is similar to Guitar Hero and Rock Band by Harmonix.  You can make your own Clone Hero charts.  You can play Clone Hero with a guitar controller, midi drum kit and more. This just like Step Mania is something that we should all aspire towards.  I would love to see tokenized Clone Hero charts.  This is how we make the metaverse real by fixing the problems of old dlc.



## About Redundant Traits

There are a lot of traits in the metadata template that are redundant, meaning the same thing is written in more than one place. &#x20;

For example "name" and "title" will always have the same thing. Some of the redundant traits are duplicated into the Attributes so they show up on the marketplaces, but they're still kept in the normal non attribute form because the attributes array is a pain in the ass to deal with in my opinion.

Another example is written about above with the Audio traits being "animation\_url", "audio\_url", "lossless\_audio", "mp3\_url", and "lossy\_audio".



