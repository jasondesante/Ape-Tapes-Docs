---
description: The rebuild update
---

# Alpha 3.0

Alpha 3.0 is a rebuild rather than a feature drop. The whole codebase moved to TypeScript, the data layer became its own open source package, and every major page got redesigned.

## Full TypeScript Conversion

The site is now TypeScript in strict mode across 1,370 files. The only JavaScript left in the source tree is test files.

The conversion went further than renaming files:

* Factory closures like `SubjectFunctions()` became real hooks
* Every component became a named function declaration, so code maps can see them
* Context consumers moved to null-safe custom hooks (`usePlayerContext()`, `useArweaveContext()`, and the rest) instead of raw `useContext()` calls
* `strictNullChecks` and `noImplicitAny` are on

It took months and touched almost every file. Nothing about it is visible from the outside, which is the point. It makes everything after it faster to build and much harder to break.

Route-level code splitting landed alongside it and cut the bundle the browser downloads up front by about two thirds.

## The Playlist Data Engine

The code that reads playlist data is now [`playlist-data-engine`](../../create/build-your-vision/playlist-data-engine.md), an open source package on npm. Anyone can install it and build on Serverless Playlists without writing the parsing, the gateway failover, or the audio analysis themselves.

It also does considerably more than parse. Beat detection and rhythm game charts, ML genre and mood classification, pitch detection, color extraction, and an RPG layer that turns any song into a character, an enemy, and a combat encounter.

Every feature has a working demo in the [Playlist Data Showcase](../../create/build-your-vision/playlist-data-showcase.md).

The site runs on it. Playlist metadata, Arweave gateway resolution, embedded player accent colors, and archive-wide genre analysis all go through the package now, so anything you build with it runs the same code the player runs.

## The Directory

A large researched list of tracks pulled from the older music NFT platforms. It is a project of its own and gets its own write-up. The full story is on the [Explore page](https://listen.arweave.net/#/explore/the-directory).

## UI Redesign

Every major surface got rebuilt.

* **Welcome page** — four tabs (Listen, Create, Collect, Learn) with live embedded players
* **Explore page** — a feed of articles, videos, posts, and tools at `/explore`
* **Contract Wizard** — new layout and dialogue system
* **Contract Manager** — new interface with a full modal suite
* **Metadata Maker** — modular form tabs with a sidebar that tracks progress and jumps between sections
* **Promos page** — new card UI
* **Stats & Achievements** — the Records and Achievements pages merged into one tabbed page, opened from the wallet menu
* **Store and Copies** — global search, toggleable sort directions, grouped grids
* **Arweave Feed** — browse uploads as 3D crates
* **Playlists** — cover uploads, generated collages, a paginated gallery, and an add-to-playlist drawer
* **Wallet** — pick an avatar from your collection, or set any song's artwork as your avatar

A global modal design system runs underneath all of it, so dialogs look and behave the same everywhere.

## Playlist Metadata v0.4

The playlist standard moved to v0.4. Fields are snake_case, tracks carry `artwork_url` and `tx_id`, entries can pin a `selected_mix`, playlists record the `platform` they came from, and `Playlist-Type` replaced the old remix flag with `new`, `remix`, `ep`, `lp`, and `single`.

See [Playlist Objects](../../curate/playlists/playlist-objects/) and [Playlist Tags](../../curate/playlists/playlist-tags.md) for the full spec.

## Fixes and Improvements

Hundreds of them. The ones worth naming:

* Offline audio cache with a viewer for managing what is stored
* Automatic recovery for interrupted Arweave uploads
* Native IPFS CIDv1 computation, replacing the nft.storage dependency
* AR.IO testnet support in the Turbo bundler, and cross-chain credit funding
* Custom API keys to bypass rate limits during token indexing and RPC calls
* Lossless audio prioritized when extracting a track's best source
