<div align="center">

<img src="assets/logo.png" width="112" alt="LinkPilot logo" />

# LinkPilot

### The fast, modern download manager for Windows

Files, videos, music and torrents: one app, at full speed.

[![Latest release](https://img.shields.io/github/v/release/AdhamHammam2023/LinkPilot?style=for-the-badge&color=f27a12&label=version)](https://github.com/AdhamHammam2023/LinkPilot/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/AdhamHammam2023/LinkPilot/total?style=for-the-badge&color=2ea043)](https://github.com/AdhamHammam2023/LinkPilot/releases)
![Windows 10 / 11](https://img.shields.io/badge/Windows-10%20%7C%2011-0078d4?style=for-the-badge&logo=windows11&logoColor=white)

<br />

<a href="https://github.com/AdhamHammam2023/LinkPilot/releases/latest">
  <img src="https://img.shields.io/badge/⬇%20%20Download%20LinkPilot-for%20Windows-f27a12?style=for-the-badge&labelColor=1f2937" height="48" alt="Download LinkPilot for Windows" />
</a>

<br /><br />

<img src="assets/downloads.png" alt="LinkPilot downloading files and videos" width="900" />

</div>

---

## Why LinkPilot?

<table>
<tr>
<td width="50%" valign="top">

### ⚡ Uses all of your bandwidth
Every file is split across up to **32 connections**. The speed booster keeps adding connections while the speed rises and adds more again if a server slows down mid-download. Pause, resume after a crash or a reboot, and pick up exactly where you left off.

</td>
<td width="50%" valign="top">

### 🎬 Video from almost any site
YouTube, TikTok, Facebook, Instagram, X, Vimeo, Dailymotion, Pinterest and thousands more, **from 144p up to 8K**. Get MP3 at 320 kbps, subtitles, chapters or just a clip of the video, and record live streams. It even reads the video players on movie and series sites.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🔎 Search and download
Type a song or video name: LinkPilot searches YouTube, SoundCloud and Dailymotion together and gets it as **MP3 320** or video in one click. It also handles Spotify songs, albums and podcasts.

</td>
<td width="50%" valign="top">

### 🧲 Torrents built in
Magnet links and .torrent files, with no extra app needed. **Watch a video while it downloads**, pick only the files you want, and stop seeding when it finishes.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🌐 Works with your browser
The extension for **Chrome, Edge and Brave** (Opera and Firefox too) sends browser downloads to LinkPilot and puts a download button just above any video. Alt + click any link to grab it.

</td>
<td width="50%" valign="top">

### 🔄 Always up to date
LinkPilot checks for new versions every two hours and tells you the new version number in a Windows notification. You can update in one click, or let it install by itself. Its video tools update on their own too.

</td>
</tr>
</table>

---

## Screenshots

<div align="center">

**Pick any quality, from 144p to 8K, with the size of each one**

<img src="assets/quality.png" alt="Quality picker" width="820" />

<br /><br />

**Search and download: songs and videos from several sites at once**

<img src="assets/search.png" alt="Search and download" width="820" />

<br /><br />

<table>
<tr>
<td align="center"><b>Light theme</b><br /><img src="assets/light.png" alt="Light theme" width="420" /></td>
<td align="center"><b>Full Arabic interface (RTL)</b><br /><img src="assets/arabic.png" alt="Arabic interface" width="420" /></td>
</tr>
<tr>
<td align="center"><b>Simple settings</b><br /><img src="assets/settings.png" alt="Settings" width="420" /></td>
<td align="center"><b>Proxies, speed rules and data allowance</b><br /><img src="assets/connection.png" alt="Connection settings" width="420" /></td>
</tr>
</table>

</div>

---

## Everything it can do

| | |
|---|---|
| **Downloads** | Up to 32 connections per file · smart speed booster · resume after crashes and restarts · queues and scheduler · link renewal when a link expires · checksum checks |
| **Video & audio** | 144p → 8K · MP3 / M4A / FLAC / WAV · subtitles (and Arabic subtitles) · chapters · download part of a video · live recording · playlists and whole channels · SponsorBlock |
| **Music** | Search by name · Spotify songs, albums and podcasts · identify a song and fix its tags and cover |
| **Sources** | HTTP/HTTPS · torrents and magnets · FTP, FTPS, SFTP · Google Drive · MEGA · mirrors · site grabber · RSS and watched pages |
| **After download** | Extract archives · convert video/audio · Whisper subtitles · VirusTotal scan · run a script · shut down or sleep when done |
| **Control** | Speed limits by time of day · game & call mode (lowers speed while you play or call) · monthly data allowance · per-site proxy |
| **Privacy** | Private downloads · app lock · cookies stay on your PC and are only used for sites you allow |
| **Comfort** | Arabic & English · dark & light themes · cards or list view · clipboard watching · statistics · local API and command line |

---

## Install

1. Download **`LinkPilot_x.y.z_x64-setup.exe`** from the [latest release](https://github.com/AdhamHammam2023/LinkPilot/releases/latest).
2. Run it. No admin rights needed.
3. **Windows SmartScreen** may warn you because the app isn't code-signed yet: click **More info → Run anyway**.
4. Optional: open **Browser integration** in LinkPilot and follow the steps to add the browser extension.

> **Requirements:** Windows 10 or 11 (64-bit). LinkPilot downloads its video tools (yt-dlp, FFmpeg, Deno) from their official sources the first time you need them, and checks each one's SHA-256.

## Updates

Already have LinkPilot? You don't need to come back here. From version **0.2.0**, LinkPilot finds new versions by itself and shows a notification with the new version number. Choose **Settings → Updates → Auto** to have them installed without asking.

*If you have version 0.1.0, install the latest release once by hand. Every update after that arrives automatically.*

---

<div align="center">

Built with [Tauri](https://tauri.app) · Rust · Svelte. Video support by [yt-dlp](https://github.com/yt-dlp/yt-dlp) and [FFmpeg](https://ffmpeg.org), torrents by [librqbit](https://github.com/ikatson/rqbit).

Made by **Adham Hammam**

</div>
