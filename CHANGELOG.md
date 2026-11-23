# Changelog

All notable changes to LinkPilot. The newest version is at the top.
Download any version from [Releases](https://github.com/AdhamHammam2023/LinkPilot/releases).

## [0.6.1] — 2026-11-23

- **New recording panel** — Pick the kind, the quality (YouTube, up to 4K) and the sound quality, then "Start recording". While recording: big timer, pause / resume, save, start over, cancel. Opening another video ends the recording and saves what was recorded of the first one. The bar's ✕ hides it on the current video only (it used to hide the whole site) and is not shown while recording; a site hidden earlier gets a "show the button again" button on the popup's first page.
- **Fix: "Requested format is not available"** — A picked format number that YouTube no longer offers at download time falls back to the best format at the same height.
- **Chapters: one file or one file each** — Several picked chapters or parts can be joined in order or kept as separate files; separate files each get their own row in the list.
- **YouTube recordings from the original video** — On sites LinkPilot downloads from (not live streams), ● notes the parts that play; Save downloads exactly those time ranges from the source at the chosen quality with yt-dlp and joins them into one file (FFmpeg concat). No browser encoding, so no dropped frames and no sound drift, even at 1440p/4K. Live streams and other sites still record in the browser.
- **Sound quality for recordings** — 128 / 192 / 256 / 320 kbps, remembered; used for the MP3 and for the sound of video recordings.
- **Fix: several chosen chapters downloaded as one chapter (or the wrong one)** — Each chapter became its own file and the list showed only the first.
- **Pause a recording and go on from anywhere** — While recording, ● above the video offers “Pause” (⏸ REC; go to any part of the video) then “Resume recording from here” in the same file, or “Save the recording”. Seeking and buffering pause the recording too, so files have no frozen frames.
- **Record YouTube at any quality up to 4K** — On YouTube the Record tab lists the video's qualities (from the player); picking one switches the player before recording. 1440p and 4K now record (they ask the encoder for H.264 level 5.1; level 4.0 stopped after two seconds). Sound only shows its quality: MP3 at 192 kbps.
- **Fix: recording stopped after 3 seconds with “open LinkPilot”** — After an extension update, open tabs kept the old video bar, cut off from the extension (recording and the quality list failed). The old bar now removes itself and the extension injects a working one into open tabs. Failed pieces are retried and the real reason is shown.
- **Smoother recording** — Pieces are encoded by the browser off the page's thread and sent every second, so the video no longer stutters while recording; the record button pulses smoothly. The “saved” message names the folder.

## [0.6.0] — 2026-11-21

- **Record from the video bar** — A red ● button next to MP3 records what a page is playing, on any site, at the playing quality: picture and sound, sound only (saved as MP3) or picture only. A ● REC timer and a stop button show while it records; recordings go to “LinkPilot Recordings”, get a proper duration and seek index (FFmpeg, no re-encoding) and appear in the download list. On a live stream the Record tab also lists the stream's qualities to record from now with yt-dlp. Protected (DRM) videos cannot be recorded.
- **Simple mode** — Shows only the everyday buttons (new download, video, downloads, search, help); everything else stays hidden and keeps working. Switch in the side menu or Settings → General; new installs choose on the welcome screen. Existing users keep the full interface.
- **Updates reach you** — A new version is announced in four places until it is installed: a Windows notification that stays on screen, a bar at the top of the window, “Update now” in the tray menu and a bar in the browser extension's popup. LinkPilot checks 20 seconds after it opens (was 90).
- **Faster first video lookup** — yt-dlp and Deno are started once in the background when LinkPilot opens and after they update, so the first lookup after a reboot no longer waits for Windows to scan them (measured: 82 s before, a few seconds now).
- **Fix: the WhatsApp status button was missing on a contact's first status** — WhatsApp plays it from its own stream address (served in pieces); the extension now reads every piece and saves the whole video.
- **Local addresses never go through the proxy or VPN.**

## [0.5.1] — 2026-11-16

- **Every device on your router** — In Share, “Find devices” lists every device on the same router (name, type, maker), even without LinkPilot. A phone with the LinkPilot page open receives files and saves them by itself; a new phone is invited with a QR code or WhatsApp; a smart TV plays a video, song or photo it is sent (UPnP/DLNA); a Windows computer receives files in one of its shared folders. To show makers, LinkPilot downloads Wireshark's public maker list once a month; nothing about your network is sent.
- **Your phone stays connected** — Each phone gets its own lasting key the first time it opens the page, so stopping and starting sharing, restarting the computer or making a new link no longer needs a new scan; the page reconnects by itself. The same port answers both http and https, so a saved link keeps working whatever the encryption setting. “Paired devices” lists them; “Forget” removes one. The phone page has the real logo, clearer icons and numbers that read correctly in Arabic.
- **“For the phone” arrives once, and fast** — A plain file is downloaded by the phone itself; a video or sound that is one file (MP3 included) is streamed through the computer to the phone while it downloads, over 12 connections at once, and nothing is kept on the computer. Qualities that need merging are still prepared on the computer first.
- **Progress on the taskbar icon** — While something downloads, LinkPilot's taskbar button shows how far all running downloads have got.
- **Fix: the video download bar disappeared after an extension update** — Chrome and Edge drop the extension's registered scripts on every update; the extension now registers them again on start. A release check now loads the extension, updates it and confirms the bar still appears.
- **Fix: “ads.json: Rule with id 24 was skipped”** — That ad rule's pattern was over Chrome's 2 KB limit; it is smaller now and every rule is checked before a release.
- **Fix: chosen parts of a video as MP3 failed** (“Could not extract the video from this page”) — the cut was encoded as MP3 inside an .m4a file; it is now cut in the source format and converted afterwards.

## [0.5.0] — 2026-11-15

This release also carries everything from 0.4.1 below (the stronger ad blocker with the uBlock Origin / AdGuard lists, pop-up modes, the video button settings and the live VPN notifications), which was never published on its own.

- **Share files with your phone and other computers** — A new “Share” button shows a QR code. Scan it with the phone camera and a page opens where you send files or whole folders to the computer and download what you shared, over the same Wi-Fi with no internet. Transfers resume after a dropped connection, the link is encrypted (HTTPS with a self-signed certificate; the phone's browser warns once) and each transfer shows its speed. Other computers running LinkPilot are found on the network and receive files after they accept.
- **Save WhatsApp statuses** — Turn on “Save WhatsApp statuses” in the browser extension, open WhatsApp Web and view a status: a “Save to LinkPilot” button saves the picture or video into a “WhatsApp Status” folder and lists it with your downloads. The extension asks for access to WhatsApp Web only.
- **Internet speed test** — Measures delay, jitter, download and upload through the connection LinkPilot uses (so with the VPN when it is on), with a live number, a graph and a plain verdict.
- **Diagnose a failed download** — ⋮ → “Diagnose” checks the internet, the server's name, the server's answer, resume support, free space and whether the file changed, tells you the likely cause and offers a one-click fix.
- **Fix: several parts of one video** — Picking two chapters or two far-apart parts saved only one, because both parts had the same file name. Each part is now its own file named with its time range.
- **Fix: sound parts start exactly where asked** — A part of a sound or song could start a little early or late; it is now cut precisely.

## [0.4.1] — 2026-11-09

- **An ad blocker as strong as uBlock Origin and AdGuard** — The extension now downloads the same filter lists (uBlock Origin's lists, AdGuard Base and Popups, EasyList, EasyPrivacy, Peter Lowe's list and the Arabic Liste AR) and updates them daily: more than 120,000 rules that block ads and trackers, hide them in the page (including advanced :has-text / :upward filters) and run scriptlets that switch off ad code and blocker detectors. More lists (Russian, Turkish, French, Spanish, German, mobile ads, annoyances) can be turned on in Protection → Filter lists.
- **Pop-ups: block all, ads only, or none** — A new choice in the Protection tab.
- **The video download button, your way** — Size (70–160%), language (Arabic, English, French, Spanish or automatic) and side (left, right or automatic) in the extension settings.
- **A much stronger ad blocker** — Requests to ad servers and trackers (analytics, session recording, Facebook and TikTok pixels, phone makers' telemetry) now fail outright. On ad-blocker test sites the score went from 7 to 126 of 130 (adblock.turtlecute.org) and from 63 to 433 of 482 (superadblocktest.com). A site that shows “turn off your ad blocker” still switches to stealth mode by itself.
- **Ads covering the video disappear** — Aggressive ad networks that change domains every few days (the ones on streaming servers) are recognised by the shape of their address and blocked, even in stealth mode. Boxes and layers drawn over the page are hidden automatically, the page is no longer sent to an ad when you click the video, and pop-ups through hidden frames are stopped.
- **Sites that insist on their pop-up** — When a site says “pop-ups are blocked, please allow them”, the extension reloads the page once by itself; from then on the pop-up opens in the background for 3 seconds and closes by itself while you stay on the site.
- **The browser follows the VPN by itself** — Turning the VPN on or off in the app shows a browser notification with the country and IP you now appear from, and the VPN card in the extension updates while it is open.

## [0.4.0] — 2026-11-09

- **The VPN now works even where VPNs are blocked** — WARP now connects the way Cloudflare's official app does (MASQUE on port 443), so to the network it looks like ordinary browsing. It tries HTTP/3 first and switches to HTTP/2 over a normal connection by itself if that is blocked. This fixes “Could not connect” on lines that block WireGuard.
- **Stealth mode: ads blocked, and the site never knows** — If any site shows “please turn off your ad blocker”, the extension notices by itself and switches that site to stealth mode: ads load in the background so the site thinks they ran, but you never see them, and pop-ups stay blocked. Ad images are no longer swapped either, so sites like CimaNow no longer detect the blocker.
- **Pop-ups and betting pages really get blocked** — The pop-up guard did not start after the update; that is fixed. It now recognises ads by behaviour: invisible links laid over the page, a click anywhere that opens another site, ad links on ever-changing domains, and redirects ending on casino or betting pages. The counters in the Protection tab count again.
- **Sort, and select many downloads at once** — Click any column title (name, size, status…) to sort from largest to smallest or the other way. To pick several: hold the left mouse button and drag over the rows, or use “Select” / “Select all”. A fixed bar appears at the top to start, pause, delete, copy links or rename them all at once.
- **New download, Add URL and Video each do their own job** — “New download” takes any link and shows every kind of download (file, video, torrent, many links, links from a page, song search). “Add URL” is for a direct file link and opens the download window straight away. “Video” is for video sites: video or audio only (MP3), or words to search for.
- **Update notices arrive right away** — LinkPilot checks for updates every 10 minutes. If it is hidden next to the clock, a Windows notification now appears at once instead of waiting until you open it. Also fixed: the thin line of another colour on the edge of the gradient buttons.
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
