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
| Cloudflare WARP (`api.cloudflareclient.com`, `engage.cloudflareclient.com`) and the wireproxy release on GitHub | Only when you turn the built-in VPN on |
| Public relays of iroh (n0) | Only when LinkPilot Send is on: to find your contacts and your LinkPilot number; messages stay end-to-end encrypted |

## Built-in VPN (only when you turn it on)
- **Cloudflare WARP**: the first connection registers a free, anonymous WARP key with Cloudflare (no account, no e-mail). The private key stays encrypted on your computer. While connected, your LinkPilot downloads — and your browsers, if you allow it — go through Cloudflare's network, under Cloudflare's own privacy policy.
- **Your WireGuard file or proxy**: traffic goes to the provider you chose. The file and proxy password are stored encrypted with DPAPI.
- Windows' proxy setting is changed only while the VPN is on, and put back as it was when it turns off.

## LinkPilot number
- Your 9-digit number lets people ask to connect to you; nothing is shared until you accept. It can be turned off in Settings → LinkPilot Send.

## Browser extension
- The extension talks only to LinkPilot on your own computer, through Windows native messaging.
- It sends cookies only for sites you allow, so that files which need you to be signed in can be downloaded. These cookies never leave your computer.
- You can choose sites that it should never capture.
- The ad blocker works entirely inside your browser with LinkPilot's own list; it sends nothing anywhere.

## Stored data
- Your downloads list and settings: `%LOCALAPPDATA%\LinkPilot\data\`.
- Passwords and API keys in the settings are encrypted with Windows DPAPI, so only your Windows user can read them.
- The app lock stores only a PBKDF2 hash of your password, never the password itself.
- **Private** downloads are kept out of statistics and exports, and their entry is removed once the file is opened or LinkPilot exits.

## Local API
The optional local API listens on `127.0.0.1` only, so other computers can't reach it. It also refuses requests that come from web pages, which protects it against DNS rebinding.
