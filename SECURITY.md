# Security

## Supported versions
Only the [latest release](https://github.com/AdhamHammam2023/LinkPilot/releases/latest) receives fixes. LinkPilot updates itself, so staying current takes no effort.

## Reporting a vulnerability
Please **don't** open a public issue for security problems. Use [GitHub's private vulnerability reporting](https://github.com/AdhamHammam2023/LinkPilot/security/advisories/new) instead, and include:
- the LinkPilot version,
- what an attacker could do,
- the steps to reproduce it.

You'll get an answer as soon as possible, and a fix in a new release.

## How LinkPilot protects you
- **Verified updates:** every update installer is checked against the SHA-256 in the release before it runs, and is only downloaded over HTTPS from this repository.
- **Verified tools:** yt-dlp, FFmpeg and Deno come from their official releases and are checked against a SHA-256.
- **Mark of the Web:** downloaded files keep Windows' "downloaded from the internet" mark, so Windows and your antivirus treat them with care.
- **No auto-run:** programs and scripts are never started from a notification; they are only shown in Explorer.
- **Trusted callers only:** the browser host and the named pipe accept only LinkPilot's own components, and the local API listens on 127.0.0.1 only and refuses requests from web pages.
- **Encrypted secrets:** passwords and API keys are encrypted with Windows DPAPI.
