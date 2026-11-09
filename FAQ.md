# Frequently asked questions

### Windows says "Windows protected your PC". Is LinkPilot safe?
That warning comes from SmartScreen, which shows it for every app without a paid code-signing certificate. Click **More info → Run anyway**. Every LinkPilot update is also checked against its SHA-256 before it is installed.

### My download isn't using my full speed. Why?
LinkPilot opens up to 32 connections per file when the speed booster is on (Settings → Downloads). The server is often what limits the speed: some allow only a few connections per user, and some cap each connection. Also check that no speed limit, time rule, game mode or data allowance is active; the sidebar shows the limit in force and the reason for it.

### Downloads from my browser don't reach LinkPilot.
Make sure the extension is installed and that **Capture downloads from the browser** is on (Browser integration). If Internet Download Manager is installed, its network driver can catch some file types before any extension sees them, even while IDM is closed.

### A video site shows "Audio only" or no qualities.
Play the video in the browser first and then press the LinkPilot button, so the extension can see the real stream. On movie and series sites with several servers, try another server; some servers build their link only while the video plays, and a few refuse downloads completely.

### "Access denied (403)" or "link expired"
Many sites give links that expire. Use **Refresh download address** from the ⋮ menu, or turn on automatic link renewal so the extension fetches a fresh link and the download continues from the same point.

### Where are my files?
In your download folder (Settings → General). With "Save each category in its own sub-folder" on, videos go to `Video`, songs to `Music`, programs to `Programs`, and so on. Turn it off to keep everything in one folder.

### How do updates work?
LinkPilot checks this repository every two hours. When there is a new version, a Windows notification shows its number and what is new. You can update in one click, or choose **Settings → Updates → Auto** to have updates installed without asking.

### How do I use the built-in VPN?
Click **VPN** at the bottom of the sidebar and press the big circle. The first time, LinkPilot downloads its small VPN engine (usque) and creates a free Cloudflare WARP identity — no account. Your downloads (and your browsers, if you keep that switch on) then go through the tunnel. WARP keeps a location near you; to appear in a specific country, add a WireGuard `.conf` file from your VPN provider. WARP connects the way the official WARP app does (MASQUE: HTTP/3 on port 443, or HTTP/2 over TCP 443 when UDP is blocked), so to the network it looks like ordinary browsing and works even where WireGuard is blocked.

### A site still asks me to disable my ad blocker.
Open the extension, go to **Protection** and make sure the ad blocker is on, then reload the page. LinkPilot answers ad requests with empty successful responses, so most "disable your ad blocker" checks pass. If one site still complains, use **Allow ads on this site** for it, and tell us the address in an issue so we can handle it.

### What is my LinkPilot number?
It is a fixed 9-digit number, shown at the top of the **Send & chat** page — like an AnyDesk address. A friend types it and presses **Connect**; you both see the same 6-digit safety number, and you accept. After that you can chat and send files, voice notes and links, end-to-end encrypted. You can turn requests by number off in Settings → LinkPilot Send.

### Is LinkPilot free?
Yes.

### Something is broken. How do I report it?
[Open an issue](https://github.com/AdhamHammam2023/LinkPilot/issues/new/choose) and include your LinkPilot version (Settings → About) and the link that failed, if you can share it.
