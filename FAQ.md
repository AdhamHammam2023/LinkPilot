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

### Is LinkPilot free?
Yes.

### Something is broken. How do I report it?
[Open an issue](https://github.com/AdhamHammam2023/LinkPilot/issues/new/choose) and include your LinkPilot version (Settings → About) and the link that failed, if you can share it.
