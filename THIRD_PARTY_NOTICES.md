# Third-party notices — LinkPilot

LinkPilot is built with open-source components. This file lists them and the
obligations that come with redistributing them. The complete, machine-generated
lists (name, version, license, repository) are in:

* `docs/licenses/rust-crates.csv` — 529 Rust crates compiled into `linkpilot.exe` and `linkpilot-host.exe`
* `docs/licenses/js-packages.csv` — JavaScript packages bundled into the interface

They are updated with every release.

## Summary of licenses in the shipped binaries

| License family | Notes |
|---|---|
| MIT, Apache-2.0, BSD-2/3-Clause, ISC, Zlib, Unlicense, 0BSD, BSL-1.0, Unicode-3.0, CC0-1.0 | Permissive. Keep copyright notices and license texts. |
| MPL-2.0 (cssparser, cssparser-macros, dtoa-short, selectors, option-ext) | File-level copyleft. Used unmodified; their source is available at crates.io / their repositories. Any modification to those files would have to be published under MPL-2.0. |
| GPL / LGPL / AGPL | **None** in the shipped LinkPilot binaries. |

## Main components

| Component | License | Use |
|---|---|---|
| Tauri 2 (tauri, tao, wry, plugins) | MIT OR Apache-2.0 | Desktop shell |
| Microsoft Edge WebView2 Runtime | Microsoft software license (redistributable bootstrapper) | Renders the interface; installed by the official bootstrapper when missing |
| Tokio, reqwest, hyper, native-tls | MIT | Networking |
| rusqlite + SQLite | MIT + Public Domain | Database |
| librqbit 9.0.1 (and librqbit-*) | Apache-2.0 | Torrent engine |
| aws-lc-rs / aws-lc-sys (via librqbit's HTTP client) | ISC AND Apache-2.0 AND MIT AND BSD-3-Clause (see crate) | TLS for torrent trackers |
| suppaftp (MIT OR Apache-2.0), russh + russh-sftp (Apache-2.0) | see left | FTP / FTPS / SFTP downloads |
| quick-xml | MIT | RSS / podcast feeds |
| aes, ctr, base64 (RustCrypto) | MIT OR Apache-2.0 | MEGA public-file decryption |
| tauri-winrt-notification, windows | MIT OR Apache-2.0 | Notifications with buttons, Windows Hello |
| Svelte 5 | MIT | User interface |
| Simple Icons 16.35 | CC0-1.0 | Brand marks of supported sites. Trademarks remain the property of their owners; LinkPilot is not affiliated with or endorsed by them. |
| esbuild (extension build tool only, not shipped) | MIT | Build |

## Components downloaded on demand (not bundled in the installer)

When the user asks for video support, LinkPilot downloads these from their
official release pages and verifies their published SHA-256 checksums:

| Component | License | Source |
|---|---|---|
| yt-dlp (`yt-dlp.exe`) | Unlicense (public domain). The official Windows build also contains Python and other libraries under their own licenses (see the yt-dlp release's THIRD_PARTY_LICENSES). | https://github.com/yt-dlp/yt-dlp |
| Deno | MIT | https://github.com/denoland/deno |
| whisper.cpp + ggml models (optional subtitles) | MIT | https://github.com/ggml-org/whisper.cpp — models: https://huggingface.co/ggerganov/whisper.cpp |
| FFmpeg — **LGPL build only** (BtbN `win64-lgpl` static build) | LGPL-2.1-or-later | https://github.com/BtbN/FFmpeg-Builds — source: https://ffmpeg.org/download.html |
| Chromaprint `fpcalc` (optional, song fingerprints for AcoustID) | LGPL-2.1 (the Windows build includes FFmpeg under LGPL) | https://github.com/acoustid/chromaprint |

Online services used only when the user asks for them (no data is sent
otherwise): Spotify's public embed pages and, with the user's own keys, the
Spotify Web API; YouTube Music search; Apple's podcast directory (to find a
podcast's public RSS feed); MusicBrainz and the Cover Art Archive; AcoustID and
AudD with the user's own keys. Song audio is never taken from Spotify (it is
DRM-protected); songs come from their YouTube Music copy.

LinkPilot runs these as separate programs and never links them into its own
code. If FFmpeg is redistributed with LinkPilot in the future, the LGPL
requires shipping its license text and offering its corresponding source code;
`LICENSE.txt` and `SOURCE.txt` are placed next to the downloaded copy.

A user's own FFmpeg already installed on the computer (for example a GPL
"full" build) may be used for personal use when the setting "Use the FFmpeg
already installed" is on; LinkPilot never copies, modifies or redistributes it.

## Not used

LinkPilot contains no code, assets or data from Internet Download Manager or
any other proprietary download manager.
