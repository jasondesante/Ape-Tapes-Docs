# Playlist Specs

A playlist is technically just a json file, that is an array of objects.  Every track in the playlist array is an object.

## Inside A Playlist Object

Inside every playlist object are these fields

* name - The name of the playlist
* tracks - an array of objects, each object being a track.  What is inside of a track is described [below](playlist-specs.md#inside-a-track-object).
* image - the url of the image for the playlist
* creator - the wallet address of the creator of the playlist
* version - the version of the playlist metadata&#x20;

## Inside A Track Object

Inside every track object are a number of different fields. The fields that you will possibly see in a track object are:

* metadata: A stringified copy of the metadata json downloaded from the Token URI. This is by far the most important field for every track.  Inside the metadata will be the links to the picture, audio and all information about the track. &#x20;
* chain\_name: What chain the track is from
* token\_address: The address of the contract the track is from
* token\_id: The Token ID of the track
* token\_uri: The URL of the metadata
* name: The name of the contract the track is from
* symbol: The symbol of the contract the track is from
* uuid: A unique identifier for each track, for the times when the same song is in the playlist
* playlist\_index: The position in the playlist that the track is in
* platform: What platform the track is from
* contract\_type
* id: A unique identifier for each track
* title: The title of the track



These are all the possible fields you might see in a track object in a playlist array.&#x20;
