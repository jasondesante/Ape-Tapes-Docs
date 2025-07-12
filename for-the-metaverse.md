# For The Metaverse

## Infinite Players

You can make your own player for serverless playlists by reading the json of the playlist format.  You can also prompt ai to read the json for you by explaining how the data is organized.  That is what this page is about.

The regular player is great for what it needs to do, but once the playlists are made, it's a whole new world.  You can take any public playlist anywhere in the metaverse.  Playlists are an easy to understand format, and this page will make it even easier to understand.

### Try It Out

Try prompting Websim to generate a player [here](https://websim.ai/).

Try [this](https://websim.ai/c/yUo4sWe92Yiyw1t1t) one pre loaded with a playlist, or another that I generated in a couple minutes [here](https://websim.ai/c/7GHbCvRWBRs4C54Is). (Use any playlist hash, or use this hash: 26kAioACfUPgri8iHxPf7d2zoWepwFies9Gw8rarCRM if you need a quick one to test)

There's a lot of examples down here [#examples-of-players](for-the-metaverse.md#examples-of-players "mention")

## What's Inside A Playlist?

A serverless playlist is a json object with the fields detailed [here.](curate/playlists/playlist-specs.md#inside-a-playlist-object)  A playlist can have songs, videos, or anything that is a token.

## AI Prompts

### Serverless Player With AI

#### Prompt in Websim:

Can you make a json file viewer that lets me input a url and then it fetches the url and displays the json.  Make it so the url is always from "https://arweave.net/" and then I will input the Arweave hash. And it will fetch the json and display the json

Inside every link I will provide, the json will be an object with a field called tracks, which will be an array of objects. Every object in the tracks array will have a field called "metadata" which itself is a stringified json. I want you to parse that json and look inside that metadata json. In it will be a field called "title" or "name" whichever exists or that you find first I want you to use that as the name of the track and display the list of tracks.

Also in that parsed metadata json is a field called "image" which has a url to the image. There's also a song in this parsed metadata. I want you to look in "audio\_url", and then "lossless\_audio", then "mp3\_url", "lossy\_audio" and finally "animation\_url" for possible places to find a url for the audio track.

Can you please display the playlist and let me click each song and play?

## Descriptions Of Playlist Data

You can use one of these descriptions to help digital intelligence understand the playlist and where the stuff you want is.

#### Short Description of Track Name/Image/Audio

Inside every playlist file, the json will be an object with a field called tracks, which will be an array of objects. Every object in the tracks array will have a field called "metadata" which itself is a stringified json. I want you to parse that json and look inside that metadata json. In it will be a field called "title" or "name" whichever exists or that you find first I want you to use that as the name of the track and display the list of tracks.

Also in that parsed metadata json is a field called "image\_small" or "image" which has a url to the image.  Use "image\_small" if you can, if not use "image".  There's also a song in this parsed metadata. I want you to look in "audio\_url", and then "lossless\_audio", then "mp3\_url", "lossy\_audio" and finally "animation\_url" for possible places to find a url for the audio track.

#### Longer Description of Playlist Metadata

The playlist object has name for the name of the playlist, image for a url of the playlist image, creator for the wallet of the playlist creator, and tracks which is an array objects for every track in the playlist.

Tracks is an array of objects where every track has chain\_name to describe what chain the token is from.  token\_address is the contract address the token is from, and token\_id is the token id that the track is of.  name is the name of the contract the token is from, and platform describes what minting platform the token is from. The most important field of all in a track object is called metadata. &#x20;

The metadata field inside a track object inside the array of tracks inside a playlist object is itself a stringified json.  To read the metadata in the metadata field you need to parse the stringified json into a json object. &#x20;

Every track's parsed metadata has an image that can be found under "image\_small" or "image".  Please check the images in that order and use the first field that has a working url to an image.  You want to prefer "image\_small" because that image will load faster than the normal size.

The name of the song is in the parsed metadata under "name" or "title".  The artist is found under "artist".  The album will be found under "album". &#x20;

Most important is the audio file which can be found under "audio\_url" or "lossless\_audio" or "mp3\_url" or "lossy\_audio" or "animation\_url".  Please check in that order of importance and use the first audio file you can fetch.



## Examples of Players

You really can make infinite amounts of serverless metaverse compatible players with this playlist idea.  Here are some examples.

#### Winamp / Webamp

A Pikachu winamp theme player - [here](https://websim.ai/c/NeX6t7t6frczOZ25n)

A regular theme winamp player - [here](https://websim.ai/c/TKkgnknz47geYbXdG)

A Jackie Chan theme winamp player with code to embed it in to other sites - [here](https://websim.ai/c/x4kzZRONtEOD7vM6y)

#### Simple Players

A 90s Retro Cosmic Arweave Playlist Explorer - [here](https://websim.ai/c/wFUjy7DSsnL6syh9q)

Simple Memphis Milano themed Arweave playlist player - [here](https://websim.ai/c/E6CiRFD3HIQevs0QG)

A player with bouncing balls - [here](https://websim.ai/c/9u2o0g3goU0Twomwj)

#### Getting Interesting

3D VR/AR demo of a simple metaverse player - [here](https://node1.irys.xyz/hVtSQBCc8qCQsJR_CkMp8z4ovJR7jHj89XZmF51yNCM)

Generative theme park where every track in the playlist is a different rideable rollercoaster of different length - [here](https://websim.ai/c/iPH3f5nHPI0OZhmZU)

Player that lets you generate your own visualizers with a prompt - [here](https://websim.ai/c/QT6bMTSy8No66E9WP)

