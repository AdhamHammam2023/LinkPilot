# Installing LinkPilot

## Requirements
- Windows 10 or Windows 11, 64-bit
- About 30 MB of disk space for LinkPilot, plus about 150 MB for the video tools
- Microsoft Edge WebView2 (already part of Windows 11; the installer adds it on Windows 10 when it is missing)

## Install
1. Open the [latest release](https://github.com/AdhamHammam2023/LinkPilot/releases/latest).
2. Under **Assets**, download `LinkPilot_<version>_x64-setup.exe`.
3. Run it. LinkPilot installs for your Windows user only, so it needs no administrator rights.
4. If **Windows SmartScreen** shows a blue warning, click **More info** and then **Run anyway**. LinkPilot isn't code-signed yet, and that is the only reason for the warning.

LinkPilot is installed in `%LOCALAPPDATA%\LinkPilot\`, and your downloads list and settings are stored in `%LOCALAPPDATA%\LinkPilot\data\`.

## Video tools
Video downloads use **yt-dlp**, **FFmpeg** and **Deno**. The first time you need them, LinkPilot offers to download them from their official sources and checks each file's SHA-256 before using it. After that they keep themselves up to date (Settings → Video).

## Browser extension
1. In LinkPilot, open **Browser integration**.
2. Click **Open extension folder**.
3. In Chrome, Edge or Brave, open the extensions page (`chrome://extensions`, `edge://extensions` or `brave://extensions`) and turn on **Developer mode**.
4. Click **Load unpacked** and choose that folder.
5. Pin the LinkPilot icon to the toolbar.

## Updating
From version 0.2.0 on, LinkPilot updates itself; see [Updates in the README](README.md#updates). Installing a newer setup over an older one also works, and keeps your downloads and settings.

## Uninstalling
Use **Settings → Apps → Installed apps → LinkPilot → Uninstall** in Windows. Files you downloaded are never deleted.
