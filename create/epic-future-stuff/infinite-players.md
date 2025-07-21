# Infinite Players

Playlists are an easy to understand format, and this page will show you how easy it is to integrate playlists.

You can prompt any type of player into existence that supports Serverless Playlists. AGI can read the JSON for you by explaining how the data is organized.&#x20;

#### Expand Into The Metaverse

The regular player is great for what it needs to do, but once the playlists are made, you can do anything.  You can take Serverless Playlists anywhere in the metaverse. &#x20;

## Try It Out

You can create any player you want. A great way to start is to use a tool like Websim.

### Websim

Try prompting Websim to generate a player [here](https://websim.ai/). Use one of the prompts below.

Try [this](https://websim.ai/c/yUo4sWe92Yiyw1t1t) one pre loaded with a playlist, or another that I generated in a couple minutes [here](https://websim.ai/c/7GHbCvRWBRs4C54Is). (Use any playlist hash, for example this playlist: 26kAioACfUPgri8iHxPf7d2zoWepwFies9Gw8rarCRM)

There's a lot of examples down here [#examples-of-players](infinite-players.md#examples-of-players "mention")

### What's Inside A Playlist?

A Serverless Playlist is a JSON object with the fields detailed [here.](../../curate/playlists/playlist-objects/#inside-a-playlist-object)  A playlist can have songs, or videos. Any token or decentralized hosted file.

## Prompts

### Serverless Player Prompts

#### Websim Prompt 1:

{% code overflow="wrap" %}
```markdown
Can you make a json file viewer that lets me input a url and then it fetches the url and displays the json.  Make it so the url is always from "https://arweave.net/" and then I will input the Arweave hash. And it will fetch the json and display the json.
Inside every link I will provide, the json will be an object with a field called tracks, which will be an array of objects. Every object in the tracks array will have a field called "metadata" which itself is a stringified json. I want you to parse that json and look inside that metadata json. In it will be a field called "title" or "name" whichever exists or that you find first I want you to use that as the name of the track and display the list of tracks.
Also in that parsed metadata json is a field called "image" which has a url to the image. There's also a song in this parsed metadata. I want you to look in "audio_url", and then "lossless_audio", then "mp3_url", "lossy_audio" and finally "animation_url" for possible places to find a url for the audio track.
Can you please display the playlist and let me click each song and play?
```
{% endcode %}

### Playlist Description Prompts

You can use one of these descriptions to help digital intelligence understand the playlist and where the stuff you want is.

#### Description of Playlist 1 (short):

{% code overflow="wrap" %}
```markdown
Inside every playlist file, the json will be an object with a field called tracks, which will be an array of objects. Every object in the tracks array will have a field called "metadata" which itself is a stringified json. I want you to parse that json and look inside that metadata json. In it will be a field called "title" or "name" whichever exists or that you find first I want you to use that as the name of the track and display the list of tracks.
Also in that parsed metadata json is a field called "image_small" or "image" which has a url to the image.  Use "image_small" if you can, if not use "image".  There's also a song in this parsed metadata. I want you to look in "audio_url", and then "lossless_audio", then "mp3_url", "lossy_audio" and finally "animation_url" for possible places to find a url for the audio track.
```
{% endcode %}

#### Description of Playlist 2 (long):

{% code overflow="wrap" %}
```markdown
The playlist object has "name" for the name of the playlist, "image" for a url of the playlist image, "creator" for the wallet of the playlist creator, and "tracks" which is an array objects for every track in the playlist.
Tracks is an array of objects where every track has chain_name to describe what chain the token is from.  token_address is the contract address the token is from, and token_id is the token id that the track is of.  name is the name of the contract the token is from, and platform describes what minting platform the token is from. The most important field of all in a track object is called metadata.  
The metadata field inside a track object inside the array of tracks inside a playlist object is itself a stringified json.  To read the metadata in the metadata field you need to parse the stringified json into a json object.  
Every track's parsed metadata has an image that can be found under "image_small" or "image".  Please check the images in that order and use the first field that has a working url to an image.  You want to prefer "image_small" because that image will load faster than the normal size.
The name of the song is in the parsed metadata under "name" or "title".  The artist is found under "artist".  The album will be found under "album".  
Most important is the audio file which can be found under "audio_url" or "lossless_audio" or "mp3_url" or "lossy_audio" or "animation_url".  Please check in that order of importance and use the first audio file you can fetch.
```
{% endcode %}

## Examples of Players

You really can make infinite amounts of metaverse compatible players with this playlist idea.  Here are some examples using Websim.

### Winamp / Webamp Players

A Pikachu winamp theme player - [here](https://websim.ai/c/NeX6t7t6frczOZ25n)

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 12.12.39 AM.png" alt=""><figcaption></figcaption></figure>

A regular theme winamp player - [here](https://websim.ai/c/TKkgnknz47geYbXdG)

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 12.13.07 AM.png" alt=""><figcaption></figcaption></figure>

A Jackie Chan theme winamp player with code to embed it in to other sites - [here](https://websim.ai/c/x4kzZRONtEOD7vM6y)

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 12.13.27 AM.png" alt=""><figcaption></figcaption></figure>

### Simple Players

A 90s Retro Cosmic Arweave Playlist Explorer - [here](https://websim.ai/c/wFUjy7DSsnL6syh9q)

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 12.13.56 AM.png" alt=""><figcaption></figcaption></figure>

Simple Memphis Milano themed Arweave playlist player - [here](https://websim.ai/c/E6CiRFD3HIQevs0QG)

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 12.14.17 AM.png" alt=""><figcaption></figcaption></figure>

A player with bouncing balls - [here](https://websim.ai/c/9u2o0g3goU0Twomwj)

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 12.14.43 AM.png" alt=""><figcaption></figcaption></figure>

### Getting Interesting

3D VR/AR demo of a simple metaverse player - [here](https://node1.irys.xyz/hVtSQBCc8qCQsJR_CkMp8z4ovJR7jHj89XZmF51yNCM)

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 12.15.44 AM.png" alt=""><figcaption></figcaption></figure>

Generative theme park where every track in the playlist is a different rideable rollercoaster of different length - [here](https://websim.ai/c/iPH3f5nHPI0OZhmZU)

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 12.16.36 AM.png" alt=""><figcaption></figcaption></figure>

Player that lets you generate your own visualizers with a prompt - [here](https://websim.ai/c/QT6bMTSy8No66E9WP)

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-21 at 12.17.38 AM.png" alt=""><figcaption></figcaption></figure>

