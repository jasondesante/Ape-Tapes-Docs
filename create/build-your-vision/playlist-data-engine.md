---
description: The open source package that turns a playlist into anything you want
---

# Playlist Data Engine

`playlist-data-engine` is an open source TypeScript package on npm. It is the data layer behind [ar://listen](https://listen.arweave.net/), and the fastest way to build on [Serverless Playlists](../../curate/playlists/) without writing the plumbing yourself.

Hand it a playlist transaction ID and it hands back clean, structured tracks. Hand it the audio and it hands back beats, genres, moods, pitch, colors, characters, and combat encounters.

```bash
npm install playlist-data-engine
```

{% embed url="https://www.npmjs.com/package/playlist-data-engine" %}
The package on npm
{% endembed %}

{% embed url="https://github.com/jasondesante/playlist-data-engine" %}
Source, full API reference, and feature docs
{% endembed %}

## The Idea

A music player that goes beyond playing static audio. Think of how the best Nintendo games use dynamic music, different arrangements depending on what the player does. That is a whole category of experiencing recorded music and almost nobody has explored it.

The engine opens that door for any music. It listens to the track and reacts to the genre, the mood, the beats, the groove, where you are, what you are doing, the weather outside, the time of day. Five years of that idea, packaged so you can `npm install` it.

## What It Does

### Playlist Parsing

The core feature. Feed it a raw playlist JSON and every track comes back flattened into consistent field names no matter which platform it came from: `audio_url`, `audio_url_lossless`, `image_url`, `artist`, `genre`, `tags`, `duration`, `bpm`, `chain_name`.

Extras come with it. Stems, alternate mixes, VRM avatars, lyrics, visualizers, video. Pinned mixes resolve automatically, so a track set to "Extended VIP" in one playlist and the primary mix in another plays correctly in both.

One-line extractors pull whole columns out of a playlist: `getAudioUrls()`, `getTrackTitles()`, `getArtists()`, `getGenres()`, `getTotalDuration()`.

### Arweave Gateway Resolution

Every Arweave URL the engine touches goes through `ArweaveGatewayManager`. It checks a cached known-working gateway, then arweave.net, then static fallbacks in parallel, then the [AR.IO Wayfinder](https://ar.io/) pool. First gateway to pass a real HEAD check wins. When a gateway dies mid-transfer, `reportGatewayFailure()` re-resolves around it.

Nothing to configure. Your player never notices an outage.

### Audio Analysis

| Mode | What It Does | Use Case |
|------|--------------|----------|
| Sonic Fingerprint | Frequency analysis at 5%, 40%, and 70% through the track | Fast profiling, character generation |
| Full Timeline | Segment by segment across the whole song | Waveform visuals, level generation |
| Music Classification | TensorFlow.js + essentia.js genre, mood, and vibe detection | Sorting, theming, recommendation |
| Pitch Analysis | Full track pYIN detection with melody contour | Melody visuals, button mapping |

Frequency splits into bass (20-400 Hz), mid (400 Hz-4 kHz), and treble (4-14 kHz). Classification covers 400+ Discogs subgenres, 60 mood themes, and vibe metrics for danceability, energy, and valence. Models are hosted on Arweave and load directly.

`ColorExtractor` pulls a k-means color palette off the artwork, which is how the player themes itself to whatever is playing.

### Beat Detection and Rhythm Games

Beats come from the Ellis 2007 dynamic programming algorithm with multi-band onset detection and ±10ms Web Audio scheduling. From there:

* **Auto charts** — transient detection, rhythm quantization, phrase detection, then easy/medium/hard/natural difficulty variants with pitch-based button mapping for DDR, Guitar Hero, and Tap modes
* **Manual charts** — per-beat key assignment, downbeats, time signature changes
* **Live sync** — `BeatStream` scores button presses against the beat map in real time
* **Groove analysis** — pocket detection, combo multipliers, subdivision switching for practice mode

Lights on the kick, particles on the snare, a playable level out of any song. No hand-timing a single frame.

### Songs as Characters

Every track has a sonic fingerprint, and that fingerprint becomes a D&D 5e character sheet: race, class, stats, abilities, spells, equipment, appearance. Bass maps to strength, mid to the mental stats, treble to dexterity.

On top of that sits a full RPG layer: procedural enemies scaled by challenge rating, turn-based combat with a Monte Carlo simulator for balance testing, equipment with enchanting and set bonuses, XP and leveling to 20 or uncapped, a ten-tier prestige system, and content packs for registering custom races, classes, enemies, and spells at runtime.

### IRL Sensors

GPS, motion, weather, solar position, and Steam activity feed into XP multipliers. Running at night in the rain is worth more than sitting still. Severe weather triggers bonus XP. Total multiplier caps at 3.0x.

### Everything Is Seedable

Same song, same character, always. `SeededRNG` (MurmurHash V3) runs through character generation, enemy creation, combat dice, and button mapping. Same seed plus same config produces identical results, which is what makes simulations reproducible and characters permanent.

## Entry Points

Three, so you only ship what you use.

```typescript
// Default — parsing, beats, characters, combat. No TensorFlow.
import { PlaylistParser, BeatMapGenerator, CharacterGenerator } from 'playlist-data-engine';

// Gateway — Arweave URL resolution and metadata extraction on its own.
import { ArweaveGatewayManager, MetadataExtractor } from 'playlist-data-engine/gateway';

// Analysis — pulls @tensorflow/tfjs, so it is deliberately separate.
import { AudioAnalyzer, MusicClassifier, PitchAnalyzer } from 'playlist-data-engine/analysis';
```

## Code

Parse a playlist and pull data out of it:

```typescript
import { PlaylistParser, getAudioUrls, getTrackTitles } from 'playlist-data-engine';

const parser = new PlaylistParser();
const playlist = await parser.parse(rawPlaylistJSON);

const urls = getAudioUrls(playlist);      // ['https://...', ...]
const titles = getTrackTitles(playlist);  // ['Song 1', 'Song 2']
```

Classify a track:

```typescript
import { MusicClassifier } from 'playlist-data-engine/analysis';

const classification = await new MusicClassifier().analyze(track.audio_url);
// → { genres: ['techno', 'detroit-house'], moods: ['energetic'], vibes: { danceability, energy, valence } }
```

Build a beat map and score presses against it:

```typescript
import { BeatMapGenerator, BeatStream } from 'playlist-data-engine';

const beatMap = await new BeatMapGenerator().generateBeatMap('song.mp3', 'track-1');
const stream = new BeatStream(beatMap, audioContext);
const result = stream.checkButtonPress(timestamp);
// → { accuracy: 'perfect', matchedBeat, offset }
```

Turn a song into a character:

```typescript
import { CharacterGenerator } from 'playlist-data-engine';
import { AudioAnalyzer } from 'playlist-data-engine/analysis';

const profile = await new AudioAnalyzer().extractSonicFingerprint(track.audio_url);
const character = CharacterGenerator.generate(track.id, profile, track);
// → { name, race, class, level, abilityScores, hp, equipment, spells }
```

Runs in the browser and in Node. Dual ESM/CJS with full type declarations.

## How ar://listen Uses It

The site is the engine's first customer, which is the point. `MetadataExtractor` reads every track that passes through playlists, uploads, and the import tools. `ArweaveGatewayManager` resolves every Arweave URL the site touches. `ColorExtractor` sets the accent color of the embedded player from the artwork. `MusicClassifier` runs genre and mood analysis across the archive.

Whatever you build with it is running the same code the player runs.

## See It Working

Every feature above has a live demo in the [Playlist Data Showcase](playlist-data-showcase.md).

{% embed url="https://playlist-data-showcase_contractwizard.arweave.net/" %}
Live demo of the engine
{% endembed %}
