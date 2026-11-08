# Changelog

All notable changes to LinkPilot. The newest version is at the top.
Download any version from [Releases](https://github.com/AdhamHammam2023/LinkPilot/releases).

## [0.4.0] — 2026-11-08

- **A smarter ad blocker with statistics** — Sites do not notice it, so “disable your ad blocker” messages do not appear. Pop-ups a page opens without your click are stopped before they open, and a tab that bounces through ad sites is closed at once. The Protection tab shows how many ads and pop-ups were blocked, the busiest ad sites and recent activity.
- **A smarter, nicer video bar** — The bar over videos is now glassy with a gradient icon, shows the quality and length of what is playing (e.g. 1080p · 12:34 or LIVE), has an MP3 button for audio only, and confirms “Sent to LinkPilot ✓”. Site styles cannot break it.
- **VPN status in the browser extension** — The extension window was redone in the app’s colours, with a card that tells you whether the VPN is on (with IP and country) and a button to turn it on or off.
- **Right-click any download** — Right-click any row in the table for everything you can do: open, open folder, pause or resume, the download window, convert, copy link, properties and delete.
- **A clearer “Convert” button** — It opens a list of your finished videos and songs: pick one and turn it into MP4, MP3 or GIF, make it smaller, or cut a part.
- **A completely new look** — Navy colours with a purple-to-cyan gradient, a downloads table with name and address, size, progress, speed, time left and status, and a details panel below. The sidebar has the library and categories, the toolbar has an icon above each label, and search sits in the title bar (Ctrl+F). Double-click a download for its own window with a big percentage, speed limit and connections.
- **Your LinkPilot number, like AnyDesk** — Every copy has a fixed 9-digit number on the Send page. Give anyone your number, they type it and press Connect, you accept after comparing the safety number, and then you send files, links and chat — no invite code.
- **Free built-in VPN (Cloudflare WARP)** — The VPN button under the sidebar: one click and your downloads go through the free WARP tunnel, so blocked sites open — your browsers too if you want. Add a WireGuard file from any provider to pick a country, or your own proxy.
- **Ad blocker in the browser extension** — Turn it on in the extension window: it blocks ads, pop-ups, trackers and YouTube ads, and is built so sites do not notice it. You can allow ads on a site you like.
- **Video pictures in the list** — Any video or song with a picture (YouTube or any site) shows it next to its name in the table, the details panel and its download window.
- **Change connections while downloading** — In the download window → Speed limiter: the number of connections changes at once, no pause and resume.
- **.torrent files and magnet links open with LinkPilot** — Double-click a .torrent file or click a magnet link in the browser and it opens in LinkPilot (when no other torrent program is set). You can also pick it from “Open with” or Windows Default apps.
- **Video button: small style and opacity** — In the extension window pick a small button (↓ and ✕ only) and set its opacity. Closing it with ✕ keeps it closed on that site, and it hides in full screen.
- **Deleting really stops the download** — Pressing ✕ and closing LinkPilot used to leave the download running in the background and bring it back later. Now it stops at once, you get 10 seconds to Undo, and closing LinkPilot carries out the deletion.
- **More fixes and improvements** — If LinkPilot freezes, starting it again offers to close and restart it. A clear message when the download drive is locked by BitLocker. The window remembers its size and place. The browser extension updates itself after every LinkPilot update.

## [0.3.1] — 2026-11-02

### Chat like WhatsApp Web
- **Ticks**: one tick = sent, two = delivered, two green = read (read receipts can be turned off). Messages to someone offline wait and are **delivered automatically** when they open LinkPilot.
- **Online / last seen / typing…** in the chat header, **profile pictures** shared with your contacts, unread counters, day separators and animations.
- **Drag and drop** files onto the chat or **paste** pictures; a **preview tray** lets you add or remove files and write a caption before sending. Pictures and videos show inside the chat.
- **Voice notes** with a waveform of the real sound and their length.
- **Link cards** (picture, title, site) for YouTube and any site or server; clicking a link offers **Open in browser / Show qualities / Download now**.
- **Delete for me** or **Delete for everyone**, emoji, copy, show in folder.
- **Notifications with sound** for every new message (Settings → LinkPilot Send), and different sounds for sending and receiving.

### Other new things
- **Hear the sound while picking a part** of a video before downloading.
- **French and Spanish** interface.
- **Downloads and Completed on one page** (the separate Completed page is gone).

### Fixes
- Updating failed with “File not found on the server” (the 0.3.0 release had a different tag); the installer is now also fetched from the latest release, and LinkPilot checks for updates **every 10 minutes** — at once when a chat contact already has a newer version. Copies set to automatic updates that failed used to stay silent; they now show the update window.
- “Open” in the chat showed “Invalid save location”; messages stayed on “sending”; closing the file prompt refused the file.
- Server details and top speed of video downloads now show from the start (not only after pause/resume).
- Audio bitrates sit next to the format in the quality window; the Downloads toolbar no longer sticks out of its card; the side menu's scrollbar no longer shows outside the menu in Arabic.

## [0.3.0] — 2026-11-01

### LinkPilot Send — send and chat with anyone, anywhere
- New **Send & chat** page: connect with a friend using an **invite code** and a **6-digit safety number** you both compare, then send **files, videos, voice notes, links, magnets and .torrent files** and **chat** — even across cities and countries, one-to-one or in **groups of up to 10**.
- End-to-end encrypted: devices connect directly and use a relay only when there is no direct path; a relay cannot read anything.
- Safety settings: who can send to you, **ask every time or only the first time**, allowed kinds, size limit, blocking. Broken transfers continue where they stopped, every file's fingerprint is checked, programs are scanned with Defender.

### Library and watching
- New **Library** page: search, automatic categories (video, series, music, documents, programs…), your own labels, and **duplicates found by fingerprint**.
- **Watch** shelf: continue watching, series grouped by season and episode, posters made from the videos, and a **built-in player** with subtitles, speed and picture-in-picture.
- **Search inside subtitles** and jump to that moment. **Free up space**: big old files to the Recycle Bin, or **shrink videos to H.265 on the graphics card** while the computer is idle.

### File hosts and servers
- **MediaFire, Pixeldrain, 1fichier, Terabox and Google Drive folders**: the real file without waiting pages; folder links list every file. **Metalink** (.meta4) downloads from all mirrors with a hash check.
- Every download shows **the server it comes from** (Cloudflare, Google, Akamai, MediaFire…), its city when known, IP address and **top speed**.

### Smarter downloads
- Pauses when the **internet drops** and continues by itself; **metered network** (phone hotspot) limit or pause; **battery** pause; continues on another drive when one is full.
- **YouTube throttling watchdog**: a slowed-down video gets a fresh link and continues. Speeds can be shown in **Mbit/s** like internet plans.
- **Connection check** page (why is it slow?), **DNS over HTTPS**, log export.
- **After-download rules** (move, label, convert, compress, extract, open), **watch folder**, **webhook**.
- **Subscriptions** show what is new by name, with **Download / Skip** when automatic download is off; **live streams are recorded as soon as they start**; torrent RSS, IP blocklist, seeding ratio and hours.
- **Search** keeps loading results as you scroll — no limit.

### Everyday use
- **Ctrl+K** command palette, custom shortcuts, a small floating window of running downloads, **Undo** after delete, download templates, batch rename, warnings for disguised files (.pdf.exe), file integrity check, loudness normalize / noise clean-up, description and comments saved with videos.
- Animated welcome screens for new users and this animated **What's new** window.

### Windows 32-bit
- New **32-bit installer** (`LinkPilot_0.3.0_x86-setup.exe`) for older PCs. Video components: yt-dlp is available in 32-bit; FFmpeg, Deno and Whisper have no 32-bit builds, so merging high qualities, subtitles creation and some YouTube formats need your own 32-bit FFmpeg — or the 64-bit LinkPilot.

## [0.2.3] — 2026-10-26

### Playlists
- New **Put them all in one ZIP file** in the playlist window. When every video has finished, they are packed (with their subtitles) into one ZIP named after the list, next to its folder. **Delete the separate files once the ZIP is ready** keeps only the ZIP. Closing LinkPilot halfway is fine: it finishes the ZIP the next time it runs.

### Downloads
- New **Select** on the Downloads and Completed pages: tick several downloads (or **Select all**) and **Delete selected** in one go, with the option to delete the files from disk too.
- New **Delete all** on the Downloads page.

### Updates
- After an update LinkPilot now **opens again by itself** and shows **What's new** in the app's language (Arabic or English).
- New choice in Settings → Notifications: **Show update alerts** inside LinkPilot, as a Windows notification, or both.
- LinkPilot now checks for a new version every half hour instead of every two hours.

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
