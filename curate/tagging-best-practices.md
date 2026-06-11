---
description: The conventions that make Arweave music tags actually work.
---

# Tagging Best Practices

If you're building your own uploader, player, or anything that reads or writes music tags on Arweave — this page is for you. Following these conventions ensures your files show up in search results and work across all D.A.M.N. apps.

## The Most Important Rule: Lowercase Values

**Every custom tag value must be lowercase.** This is not a suggestion.

Arweave tags are exact-match. That means `"Rock"` and `"rock"` are **completely different values**. If you upload a file with `Genre: Rock` and someone searches for `Genre: rock`, it will not show up. Your file becomes invisible.

### Why This Matters

* **Arweave is permanent.** Once it's uploaded, you can't edit the tags. If you upload with mixed case, that data is stuck that way forever.
* **Search is case-sensitive.** The Arweave GraphQL API does exact matching on tag values. There is no "case insensitive" mode.
* **It fragments the library.** If one person uploads with `Genre: Electronic` and another with `Genre: electronic`, those are two separate genres now. The whole point of tagging is to create a shared, searchable library.

### What Gets Lowercased

* `Title` values → lowercase
* `Artist` values → lowercase
* `Genre` values → lowercase
* `Search-Tag` values → lowercase
* All custom tag values → lowercase

### What Doesn't Get Lowercased

* `ISRC` — This is an exact code (e.g., `USRC17607839`) and must be preserved exactly as provided.
* System tags like `Uploaded-Type`, `App-Name`, `Playlist-Version` — These have fixed values that never change.
* `Image` — This is an Arweave transaction ID which is case-sensitive.

### The Performance Benefit

Lowercase values don't just prevent mistakes — they're faster. When all values are lowercase:

* Searching is faster because the indexer doesn't need to handle case variations
* Queries are simpler — you always search lowercase
* Results are more complete — you catch everything instead of missing uploads with different casing

## Always Include These Tags

### For Audio Files

```
Uploaded-Type: Audio
App-Name: Contract-Wizard
```

`Uploaded-Type: Audio` is how all audio files and audio metadata are found. If you don't include this tag, your file won't show up in any audio search.

### For Playlists

```
Uploaded-Type: Playlist
Playlist-Version: 0.4
App-Name: Contract-Wizard
```

`Uploaded-Type: Playlist` is how all playlists are found. The version tag tells players what structure to expect.

## Use Search-Tag for Everything

The `Search-Tag` tag is a unified search field. Instead of needing separate queries for Title, Artist, Genre, and custom tags — you can search `Search-Tag` once and match against all of them.

When uploading, you should:

1. Add the specific tags (Title, Artist, Genre, etc.) with their proper tag names
2. **Also** add each value as a `Search-Tag` entry

For example, a track with artist "Radiohead" and genre "alternative" would get:

```
Artist: radiohead
Genre: alternative
Search-Tag: radiohead
Search-Tag: alternative
```

There can be multiple `Search-Tag` entries on a single transaction — one for each value you want searchable.

### What Goes Into Search-Tag

For **audio files**: Title, Artist, Genre, and any custom tags.

For **playlists**: Title, Genre, any custom tags, and Artist (if the playlist type is ep, lp, or single).

## The Image Tag

The `Image` tag is optional and holds a raw Arweave transaction ID:

```
Image: abc123def456...
```

**Do not** include a gateway URL or `ar://` prefix. Just the raw tx_id. Consumers know it's on Arweave already.

## Playlist Types

Playlists should include a `Playlist-Type` tag. The values are:

| Value | When to Use |
|-------|-------------|
| `new` | A new original playlist (default) |
| `remix` | A remix of an existing playlist — also add `Original-Playlist` with the original's tx_id |
| `ep` | Extended Play release — also add `Artist` tag |
| `lp` | Long Play release — also add `Artist` tag |
| `single` | Single track release — also add `Artist` tag |

## Quick Reference

| Tag | Format | Required |
|-----|--------|----------|
| `Uploaded-Type` | `Audio` or `Playlist` (capitalized) | Yes |
| `App-Name` | `Contract-Wizard` | Yes |
| `Title` | lowercase | Recommended |
| `Artist` | lowercase | Optional |
| `Genre` | lowercase | Optional |
| `Search-Tag` | lowercase, multiple allowed | Recommended |
| `Image` | raw Arweave tx_id | Optional |
| `ISRC` | exact case (case-sensitive code) | Optional |
| `Playlist-Version` | `0.4` | For playlists |
| `Playlist-Type` | new/remix/ep/lp/single | For playlists |

## Summary

* **Lowercase everything** except ISRC and system tags
* **Always include** `Uploaded-Type` and `App-Name`
* **Use Search-Tag** to make your files discoverable with a single query
* **You can't fix it later** — Arweave is permanent, so get it right the first time
