# AionMarket

Minimal Windows x64 market widget for **AION2 Steam Global EU — Ludra, Asmodian**.

## Get started

Download **AionMarket-portable-win-x64-1.0.1.0.zip** from [the latest release](https://github.com/SkyPwner/AionMarket-Releases/releases/latest), extract the entire ZIP into a writable folder, and open **AionMarket.exe**. Python and.NET are included. First connection uses your own Steam/game session and installed Wireshark/TShark plus Npcap; official downloads are linked in the wizard. Do not use the update-only ZIP for a first installation.

## Widget and main window

The compact widget shows item icons, current observed listed unit prices and source age. Its cog opens Watchlist, History and Changelog. Search/category/rarity filters choose tracked items; source refresh is10–60seconds. Main-window Settings opens appearance/behavior preferences; the installed version, Check for updates and real update status are visible there. The Windows tray offers Show/Hide, settings, connection, updates and Exit.

History reports rolling24h minimum, unweighted mean and maximum of observed lowest listed prices, sample count/span and a chart/log preview of up to120 evenly sampled observations. Statistics use all accepted samples. Completed sales and individual highest offers are not supplied by this endpoint. Gaps/full-day coverage are never implied; loading/incomplete/unavailable/scan-limit states are explicit. The selector contains83 items from a pinned catalog, not a claim of complete current game coverage.

Collection continues while the widget is hidden in the tray and the in-game market is closed. The application and game must remain running, with an awake online PC and valid session. Exit stops collection. Version1.0.1 removes the former1440-check session cap. Observations are retained locally; initial history loading costs scale with the archive. No retrospective backfill or automatic history deletion occurs. New NTFS snapshots use optional transparent compression without changing their JSON bytes; other filesystems retain normal storage.

## Local state

Settings/watchlist/history live in `%LOCALAPPDATA%/AionMarket`. Private connection material remains under `%LOCALAPPDATA%/Aion2MarketBot/private`, outside update images. No owner account session, captures, price history or personal settings are shipped. There are no automated trades, injection or game memory reads. The connection wizard starts a locally logged Steam session only after explicit user action; fully exit Steam first. Steam/game logging ends after a full normal Steam restart. Exiting AionMarket leaves Steam/game open.

## Signed updates

The portable ZIP includes `update-channel.json` containing the public ECDSA P-256 trust key and feed URL. Updates verify signed SHA256/size before staging. Check for updates, then choose Exit in the tray and reopen when ready. Game credentials are never used for GitHub update traffic. Retained state is outside versioned images.

Latest ZIP checksums: [SHA256SUMS.txt](SHA256SUMS.txt). Signed feed: [update.json](update.json). Trust descriptor: [update-channel.json](update-channel.json). Executables are not Windows Authenticode-signed; update signing is separate.

## Notices

This is a release-distribution repository. Dependency licenses and notices are included in the ZIPs. AION2 names/artwork belong to their respective owners; no ownership or redistribution license for third-party art is asserted. This is not an official NCSOFT application.
