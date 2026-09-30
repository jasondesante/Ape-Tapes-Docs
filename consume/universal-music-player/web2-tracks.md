# Web2 Tracks (YouTube)

The player plays **web2 tracks** — YouTube videos — right alongside web3 and Arweave tracks. A web2 track is marked with a red YouTube glyph wherever it appears: player-page track lists, the now-playing bar, and mobile.

## Playing a YouTube video

There are three ways to get a YouTube video into the player:

1. **Paste a link in the search bar.** Any YouTube video URL (`youtube.com/watch?v=…`, `youtu.be/…`, `music.youtube.com`, Shorts links) routes straight to the player page with that video loaded. Pasting a *playlist* link points you at the import flow instead. Everything else you type searches exactly as before.
2. **Use the deep link.** `…/#/play?youtube=<video-id or full link>` loads the video as a one-track page. Click the track to play it.
3. **Add it to a playlist.** In any created playlist's menu (⋮ → **Add Web2 Track**), paste a video link and it's appended as a track row.

## Importing a whole playlist

**Settings → Extras → Import YouTube Playlist** brings an entire YouTube playlist in as a local playlist:

1. Paste the playlist URL (or a bare `PL…` / `UU…` list id).
2. A small visible player lists the playlist's videos (first ~200).
3. Each video's metadata is fetched; unavailable videos are counted and skipped.
4. Name the playlist (prefilled from the YouTube title) and **Save as Playlist**.

The imported playlist is a normal local playlist — combinable with web3 tracks, playable, favoritable, and uploadable to Arweave like any other. Duplicate imports get a numbered suffix instead of overwriting.

## What works and what doesn't

A YouTube track is a first-class queue citizen: play, pause, seek, volume, shuffle, repeat, prev/next, favorites, and adding to playlists all work, and plays count toward your records.

A few things are structurally impossible for a YouTube track, so they're switched off:

* **The rhythm game** — charting needs the track's actual audio bytes; a YouTube stream can't be fetched, so YouTube tracks stay unchartable.
* **Embeds and webamp** — YouTube tracks never appear in embed players or the webamp queue.
* **The directory** — YouTube tracks never become directory entries.
* **Playback speed (fun mode)** — has no effect on a YouTube player.
* **Offline caching** — YouTube audio isn't downloadable, so it's never cached.

On mobile, screen-off auto-advance skips YouTube tracks (mobile browsers stop background video); a playlist made entirely of YouTube tracks stops cleanly instead of looping.

## The visualizer

The visualizer button works on YouTube tracks too. The first time you open it on one, the browser asks to share this tab's audio — that's the visualizer's sound feed. Accept once per visit and the whole scene reacts to the video: milkdrop presets, custom shaders, all of it. If the visualizer isn't listening (skipped prompt, or sharing stopped), a **Capture** button appears in its toolbar to attach it; Chrome's "Stop sharing" control turns the listening off.

Tab-audio sharing is desktop Chrome/Edge; in other browsers the visualizer opens without reacting to YouTube audio. Web3 tracks always react normally.

## Permanence

YouTube videos are centralized: they can be deleted, made private, or region-blocked at any time, and embedding can be disabled per video. A web2 track that stops working is skipped automatically with a notice — it never blocks the rest of the playlist. Arweave playlists that contain web2 tracks keep those entries exactly as they were saved; only their availability is at YouTube's mercy, never the playlist record itself.
