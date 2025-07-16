---
description: 721J Metadata Standards
---

# Token Metadata

Tracks contain the highest potential for metadata thiccness. With countless choices for where to put files and how to structure data, you can create truly unique tokens that bring your vision to life.

Use this template below for inspiration when writing metadata for a token.

Check the version of the template on GitHub with examples to see what is required for each field of metadata.

You can create your metadata files manually by hand using this template, like it was done in the olden days, or you can use The Metadata Maker and save yourself a lot of time.

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

## About Redundant Traits

There are a lot of traits in the metadata template that are redundant, meaning the same thing is written in more than one place. &#x20;

For example "name" and "title" will always have the same thing. Some of the redundant traits are duplicated into the Attributes so they show up on the marketplaces, but they're still kept in the normal non attribute form because the attributes array is a pain in the ass to deal with.

Another example is with the Audio traits being "animation\_url", "audio\_url", "lossless\_audio", "mp3\_url", and "lossy\_audio".
