# Changelog

All notable changes to ClearPlayer are recorded here.

Dates refer to App Store availability, not submission. Versions follow the numbering shown at the bottom of the app's Settings screen.

<!--
When cutting a release:
  1. Rename "Unreleased" to the version number and add the date.
  2. Start a fresh "Unreleased" section above it.
  3. Keep the headings in this order, dropping the ones that are empty:
     Added / Changed / Fixed / Removed
  4. Write entries for people who use the app, not for the diff.
     "Live streams no longer stall after a quality change" beats
     "set clearBufferOnQualityChange to false".
-->

## Unreleased

<!-- Entries for the next release go here. -->

---

## 2026.8.1 — 2026-08-28

First public release.

### Playback

- MPEG-DASH (`.mpd`) and HLS (`.m3u8`) playback, live and on demand
- ClearKey decryption, with keys read from `#KODIPROP` tags in the playlist
- Manual selection of video quality, audio track and subtitle track
- Codec, bitrate and resolution readout for the active stream
- Seeking within the DVR window on live streams, with return to live
- Picture in Picture, background audio and AirPlay
- HEVC playback where the stream provides it

### Playlists

- Multiple M3U/M3U8 playlists, from a URL or a local file
- Gzip-compressed playlists
- Channel groups taken from `group-title`
- Automatic refresh on a configurable interval

### TV guide

- XMLTV guide sources, with a user-defined priority order when several cover the same channel
- Gzip and xz compressed guides
- Automatic discovery of guide URLs from a playlist's `x-tvg-url` header, including multiple comma-separated URLs
- Full-screen guide grid, and an in-player guide over the video
- Programme details with description and timing
- Optional fuzzy channel matching for guides whose IDs do not line up with the playlist

### Xtream Codes

- Live categories and streams through the Xtream Codes API
- Credentials stored in the iOS Keychain
- Guide data through the provider's `xmltv.php` endpoint

### Sharing

- Send a playlist to another device as an end-to-end encrypted text code
- Optional *Hide URL* mode, where the recipient can watch the playlist without seeing its address

### Other

- English and Italian interface
- Crash reporting and anonymous usage statistics through Firebase
