# Changelog

All notable changes to LinkPilot. The newest version is at the top.
Download any version from [Releases](https://github.com/AdhamHammam2023/LinkPilot/releases).

## [0.2.0] — 2026-10-26

### Faster downloads
- The speed booster measures each step only after the new connections are actually streaming, grows faster (by half each step, up to 32 connections) and keeps extra connections unless they slow the download down.
- It keeps watching after it settles: if the speed falls later (a slower server node), it searches again.
- Saving to disk no longer pauses the connections. The disk flush now runs on its own, and the write buffer is ten times deeper, so the speed no longer dips every two seconds.

### Video
- New page reader for video hosts that yt-dlp does not support: StreamWish, VidTube, UpDown, Uqload, EarnVids/Filelions, Doodstream and their mirror domains. It unpacks the player script and downloads the stream with the right Referer.
- Movie and series pages are followed into their embedded player.
- The browser extension now picks the master playlist instead of an audio-only track (fixes "Audio only" on some sites).
- When a server really refuses, LinkPilot says so and suggests choosing another server.

### Browser extension
- The LinkPilot button now sits just above the video's top corner instead of on the picture, and follows the video while scrolling.
- It is hidden while a video is full screen.
- On YouTube's home, search and channel pages, the button on a playing preview downloads that video (fixes "requested format is not available: the list is empty").

### Settings
- "Save each category in its own sub-folder" is now right under the download folder in Settings → General.

### Updates
- LinkPilot now checks this repository for new versions every two hours and shows a Windows notification with the new version number, plus **Update now** and **Later** buttons.
- The video components (yt-dlp, Deno, FFmpeg) are checked every two hours instead of once a week.
- Every installer is verified against its SHA-256 before it runs.

## [0.1.0] — 2026-10-24

First public version.

- Segmented HTTP/HTTPS downloads with resume, queues, scheduler and speed limits.
- Video and audio from YouTube, TikTok, Facebook, Instagram, X, Vimeo, Dailymotion and thousands of other sites (yt-dlp), from 144p to 8K, MP3 320.
- Search and download, Spotify songs/albums/podcasts, song identification.
- Torrents and magnet links with streaming while downloading.
- FTP/FTPS/SFTP, Google Drive, MEGA, mirrors, site grabber, RSS subscriptions.
- After-download steps: extract, convert, Whisper subtitles, VirusTotal check.
- Browser extension for Chromium browsers and Firefox.
- Arabic and English interface, dark and light themes.

[0.2.0]: https://github.com/AdhamHammam2023/LinkPilot/releases/tag/v0.2.0
[0.1.0]: https://github.com/AdhamHammam2023/LinkPilot/releases
