---
description: Every engine feature, built out into a working demo
---

# Playlist Data Showcase

The showcase is a React app that demonstrates the [Playlist Data Engine](playlist-data-engine.md) feature by feature. Not screenshots or a feature list, actual working demos. Load a playlist by transaction ID and every tab starts operating on real tracks.

{% embed url="https://playlist-data-showcase_contractwizard.arweave.net/" %}
The live demo
{% endembed %}

{% embed url="https://github.com/jasondesante/playlist-data-showcase" %}
Source
{% endembed %}

## The Tabs

### Home

Landing page with playlist search, track cards, and quick actions. Start here, load a playlist, then everything downstream has something to chew on.

### Playlist

The parser, exposed. Paste an Arweave transaction ID or raw JSON, watch it fetch and parse, then browse the track list next to the raw response. This is where you check what the engine actually extracts from your playlists.

### Audio Analysis

Frequency analysis split into bass, mid, and treble, ML genre and mood classification, pitch contour graphing, and color extraction from the audio. The tab that shows you what a track *is*.

### Beat Detection

The biggest one. A four-step wizard with two modes.

Manual mode runs Analyze → Subdivide → Chart → Ready. Automatic mode runs Analyze → Rhythm Generation → Pitch & Level → Ready and builds the chart for you.

Along the way: beat maps, subdivisions (eighth notes, triplets, swing, quintuplets), a chart editor, practice mode, and rhythm game level generation with key assignment and difficulty scaling.

### Character Gen

Generate a D&D 5e character from the selected track's audio profile, with an equipment browser and enchantment system attached. Same track always generates the same character.

### Party

Every character you have generated, in a grid, with search, sorting, and party composition analysis. Your playlist becomes a roster.

### Items

Equipment management: equip and unequip, enchantments and curses, attunement locks, loot box spawning, and a creator for making your own items.

### Data Viewer

Browse everything the engine ships with. Spells, skills, features, races, classes, equipment, filtered by level, school, type, rarity, and tags, with raw JSON underneath and creators for custom content.

### Session

Listening session tracking with an animated timer, live XP accumulation, and track mastery badges.

### XP Calc

Calculate XP from every source the engine supports (base, environmental, gaming, rhythm) and tune the multipliers to see what each one contributes.

### Leveling

Character progression: stat management, level-up handling, the prestige system, and uncapped mode with custom XP curves.

### Sensors

GPS, motion, and weather integration with permission prompts, live data graphs, a mini-map, biome detection, and moon phase and day/night status.

### Gaming

Steam integration. Connect an account, see the game currently being played, and watch the genre-based XP bonus recalculate.

### Combat

Full turn-based combat: encounter generation, enemy templates, a combat log, and export.

### Balance Lab

Monte Carlo combat simulation. Run thousands of fights with seeded dice, get win rate charts, statistical analysis, and balance recommendations back.

### Settings

API keys, audio settings, logging, and privacy controls.

## How It Connects

Audio is the source of truth. Everything else is downstream of it.

```
Playlist (Arweave)
    │
    ▼
Audio Analysis ──► Sonic Fingerprint
    │                (bass/mid/treble/energy)
    │                       │
    ├──► Genre/Mood         ├──► Character Generation
    ├──► Pitch Analysis     ├──► Enemy Generation
    ├──► Beat Detection     │
    │       │               │
    │       ▼               ▼
    │   Rhythm Game ──►  Combat
    │                       │
    └──► Level Generation   ▼
                        XP & Leveling
```

Same audio produces the same analysis, the same levels, the same characters, and the same combat outcomes, every time.

## Running It Locally

```bash
npm install
npm run dev
```

The `server/` folder holds an optional Node backend for the Steam integration. Steam's API does not support CORS, so the browser cannot call it directly. The server runs the engine's `GamingPlatformSensors` in Node and exposes REST endpoints for game activity, XP bonuses, and diagnostics.
