# Track Metadata

The track metadata is the stringified JSON content inside each track object's `metadata` field. When parsed, this contains the actual audio links, artwork, and detailed track information that players use.

### Two Types of Tracks

#### Adding A Token (NFT)

When a track represents an NFT, it probably follows NFT metadata standards (like [OpeaSea's](https://docs.opensea.io/docs/metadata-standards)). The most important thing is whether the token has audio in it or not.

The audio will be checked at the most standard field `animation_url` and then also `audio_url`, `lossless_audio`, `mp3_url`, and `lossy_audio`. If nothing is found in those fields in the stringified object in the metadata field, then it won't show up in the player. **The player only shows tokens that have something in those fields.**

#### Adding A File (Direct Upload)

When a track represents a direct file upload, it won't follow any metadata standards initially. Tracks in playlists fall anywhere in the spectrum from undocumented file to thicc metadata, and it's when the file is added that it's formatted like metadata so everything works.

What happens is the raw file gets put into an object in the field `animation_url`, following the same standards as NFT metadata. But it's just a normal file with some extra info.

A file that's added to a playlist will have a JSON object created when it's added. If the track is already a metadata file, then it's already been prepared correctly and is turned into a string and added to the metadata field.

### Audio Field Hierarchy

Players check for audio in this order:

1. `animation_url` - OpenSea standard (can be audio, video, or other)
2. `audio_url` - More specific audio field
3. `lossless_audio` - High quality audio
4. `mp3_url` - Compressed audio
5. `lossy_audio` - Alternative compressed audio field

### Metadata Standards

Track metadata follows the ultimate bedrock of NFT metadata standards: the [OpenSea metadata standards](https://docs.opensea.io/docs/metadata-standards). That's where `animation_url` comes from, among other fields.

**The closer it is to thicc metadata, the better.** Rich metadata with detailed information, multiple audio formats, artwork, lyrics, and other content creates better experiences across different players and platforms.

For the complete specification of thicc music NFT metadata, see [Token Metadata Standards →](../../../create/the-metadata-maker/metadata-standards/token-metadata/) which explains the full template with fields for stems, alternate mixes, credits, VRM avatars, and much more. The template can also be found on GitHub.

{% embed url="https://github.com/jasondesante/721J-Token/blob/master/Metadata%20Templates/token_uri_template_blank.json" %}

### Example Parsed Metadata

When the stringified metadata is parsed, it might look like:

json

```json
{
  "name": "I Hate My Dick",
  "artist": "Cosmo Doris", 
  "image": "https://example.com/artwork.jpg",
  "mp3_url": "https://example.com/audio.mp3",
  "animation_url": "https://example.com/high-quality.wav",
  "attributes": [...],
  "description": "Track description..."
}
```

This parsed content is what drives the actual playback experience across the decentralized web.
