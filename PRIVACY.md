# Privacy

LinkPilot runs on your computer and keeps your data there.

## What LinkPilot never does
- It never collects telemetry, analytics or usage statistics.
- It has no accounts and no LinkPilot servers.
- It never sends your downloads list, history or files anywhere.

## What it connects to, and why
| Connection | When |
|---|---|
| The sites you download from | Every download, video lookup and search you start |
| `github.com/AdhamHammam2023/LinkPilot` | Every two hours, to check for a new version (you can turn this off in Settings → Updates) |
| GitHub releases of yt-dlp, FFmpeg and Deno | To install or update the video tools (you can turn this off in Settings → Video) |
| VirusTotal | Only if you turn it on and enter your own API key. It sends the file's **SHA-256 hash**, never the file itself. |
| AcoustID / AudD / MusicBrainz / Spotify | Only when you use song identification or Spotify features, with your own keys |
| Proxies | Only the ones you set up |

## Browser extension
- The extension talks only to LinkPilot on your own computer, through Windows native messaging.
- It sends cookies only for sites you allow, so that files which need you to be signed in can be downloaded. These cookies never leave your computer.
- You can choose sites that it should never capture.

## Stored data
- Your downloads list and settings: `%LOCALAPPDATA%\LinkPilot\data\`.
- Passwords and API keys in the settings are encrypted with Windows DPAPI, so only your Windows user can read them.
- The app lock stores only a PBKDF2 hash of your password, never the password itself.
- **Private** downloads are kept out of statistics and exports, and their entry is removed once the file is opened or LinkPilot exits.

## Local API
The optional local API listens on `127.0.0.1` only, so other computers can't reach it. It also refuses requests that come from web pages, which protects it against DNS rebinding.
