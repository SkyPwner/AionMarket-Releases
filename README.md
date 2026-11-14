# AionMarket

Minimal Windows x64 market price widget for **AION 2 Steam Global EU — Ludra, Asmodian**.

## Download and run

1. Download **AionMarket-portable-win-x64-1.0.0.0.zip** from [the latest release](https://github.com/SkyPwner/AionMarket-Releases/releases/latest).
2. Extract the entire archive into a writable folder.
3. Open **AionMarket.exe** at the root of the extracted folder.
4. Use **Connect game** to connect your own Steam/game session. First connection requires installed Wireshark/TShark and Npcap; the app links to their official downloads.

Python and .NET runtimes are included. Do not use the smaller update-only ZIP for a first installation.

## Features

- Compact item icons, current unit prices and source age.
- Watchlist with search, category and rarity filters; source polling every 10–60 seconds, subject to session availability and server responses.
- Windows tray: Show/Hide, Watchlist, App settings, Connect game, Check for updates and Exit.
- Opacity, always-on-top, position lock, start minimized and hide on close.
- Signed update downloads; choose **Exit** in the tray and reopen the application to use a prepared update.

The item selector contains 83 items from a pinned catalog; it is not a claim of complete current game coverage. Account-session expiration or missing connection data requires reconnecting. This application observes prices; it does not perform automated trades, inject code or read game process memory.

## Local data and connection

Settings, watchlist and price history stay under `%LOCALAPPDATA%/AionMarket`. Private connection material stays under `%LOCALAPPDATA%/Aion2MarketBot/private`, outside versioned app images. The distributed archive contains no owner's account session, captures, history or personal settings.

The connection wizard starts a locally logged Steam session only after the user's explicit action. Fully exit Steam before that step. Logging inherited by Steam/game lasts until a full normal Steam restart. Exiting AionMarket stops only its own feed/capture/source children and leaves Steam/game open.

## Updates and verification

The portable package includes `update-channel.json` with the public ECDSA P-256 verification key and the signed feed URL. Update packages are checked against their signed SHA-256 and size before staging. Game credentials are not used for GitHub update traffic. Retained settings/history are outside update images.

Compare downloaded ZIPs with [SHA256SUMS.txt](SHA256SUMS.txt). The signed live feed is [update.json](update.json); the public trust descriptor is [update-channel.json](update-channel.json). Update-manifest signing is separate from Windows Authenticode: the executables are not Authenticode-signed.

## Notices

This repository distributes prepared application releases. Dependency licenses/notices are included in the archives. AION 2 names and item artwork belong to their respective owners; no ownership or redistribution license for third-party artwork is asserted. This is not an official NCSOFT application.
