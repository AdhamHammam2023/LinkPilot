# Changelog

All notable changes to LinkPilot. The newest version is at the top.
Download any version from [Releases](https://github.com/AdhamHammam2023/LinkPilot/releases).

## [0.2.2] — 2026-10-26

### Playlists and channels
- **Fixed:** a playlist link kept loading for a long time. LinkPilot was looking up every video of the list one by one before showing anything. It now knows at once that the link is a list (about 3 seconds) and opens the list window.
- Big lists are fully supported: up to 20,000 videos per playlist or channel (a channel with 5,300 videos is read in under two minutes). Works with YouTube and any other site yt-dlp can read as a list (SoundCloud, Vimeo, Dailymotion…).
- One choice for the whole list: video (best, 4K, 1440p, 1080p, 720p, 480p, 360p) or audio only (M4A, or MP3 at 320 / 192 / 128 kbps). A video without the chosen quality downloads in the nearest lower one.
- New **Select from number … to …**, to download part of a long list (for example the first 200 videos), and the total length of the selected videos.
- A YouTube video link that belongs to a playlist (`watch?v=…&list=…`) now shows **Show the whole list** at the top of the video window.

## [0.2.1] — 2026-10-26

### Browser button
- **Fixed:** on a YouTube video page the button sometimes opened another video (one of the suggestions shown at the end of the video) instead of the one playing. It now always takes the video you are watching, and on the home, search and channel pages the video you are previewing.
- A slimmer bar, like the classic IDM button.
- It follows the page's language: on Arabic pages it reads "تحميل بـ LinkPilot" and sits on the video's left, away from the logo; on English pages it sits on the right.
- It stays below a site's top bar (YouTube's logo and search) instead of covering it.
- New **✕** next to it hides it on that page.

### Notifications
- The new-version notification now shows the version number and what is new, with **Update now** and **Later** buttons. Update now installs at once when the update is already downloaded.
- New switch in Settings → Notifications: "Notify me when an update is available". When it is off, the update window waits for you inside LinkPilot.
- LinkPilot no longer pops its window open by itself when it finds an update while it is in the tray.

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

[0.2.1]: https://github.com/AdhamHammam2023/LinkPilot/releases/tag/v0.2.1
[0.2.0]: https://github.com/AdhamHammam2023/LinkPilot/releases/tag/v0.2.0
[0.1.0]: https://github.com/AdhamHammam2023/LinkPilot/releases
