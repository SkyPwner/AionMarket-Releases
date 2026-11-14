# AionMarket

Minimal Windows x64 market widget for **AION2 Steam Global EU Р Р†Р вЂљРІР‚Сњ Ludra, Asmodian**.

## Get started

Download **AionMarket-Setup-1.0.3.0.exe** from [the latest release](https://github.com/SkyPwner/AionMarket-Releases/releases/latest), run it, and choose Install. The app opens a visible connection screen on a new PC. Steam and AION2 are detected automatically. Python and .NET are included. Wireshark/TShark plus Npcap are separate first-connection prerequisites, with official links and checks in the app. The full portable ZIP remains available; the update-only ZIP is for existing installations.

## Widget and main window

The compact widget shows item icons, current observed listed unit prices and source age. Its cog opens Watchlist, History and Changelog. Search/category/rarity filters choose tracked items; source refresh is10Р Р†Р вЂљРІР‚Сљ60seconds. The rounded main window has left navigation and larger controls. Settings opens appearance/behavior preferences. Version and update controls are in Changelog. History shows a selected item with Low, Average and High cards, a chart and recent prices. Averages are rounded for display; retained source values remain exact. The Windows tray offers Show/Hide, settings, connection, updates and Exit.

History reports rolling24h minimum, unweighted mean and maximum of observed lowest listed prices, sample count/span and a chart/log preview of up to120 evenly sampled observations. Statistics use all accepted samples. Completed sales and individual highest offers are not supplied by this endpoint. Gaps/full-day coverage are never implied; loading/incomplete/unavailable/scan-limit states are explicit. The selector contains83 items from a pinned catalog, not a claim of complete current game coverage.

Collection continues while the widget is hidden in the tray and the in-game market is closed. The application and game must remain running, with an awake online PC and valid session. Exit stops collection. Version1.0.1 removes the former1440-check session cap. Observations are retained locally; initial history loading costs scale with the archive. No retrospective backfill or automatic history deletion occurs. New NTFS snapshots use optional transparent compression without changing their JSON bytes; other filesystems retain normal storage.

## Local state

Settings/watchlist/history live in `%LOCALAPPDATA%/AionMarket`. Private connection material remains under `%LOCALAPPDATA%/Aion2MarketBot/private`, outside update images. No owner account session, captures, price history or personal settings are shipped. There are no automated trades, injection or game memory reads. For a fresh connection, the app offers a Steam launch. If Steam is already running, restarting it requires explicit confirmation because running Steam games may close. The app requests normal shutdown, waits at most 30 seconds and never force-kills it. Existing valid session material is reused. After a game-not-running stop, a game-presence check can resume the existing source; expired authentication requires reconnecting. Steam/game logging ends after a full normal Steam restart. Exiting AionMarket leaves Steam/game open.

## Signed updates

The portable ZIP includes `update-channel.json` containing the public ECDSA P-256 trust key and feed URL. Updates verify signed SHA256/size before staging. Check for updates, then choose Exit in the tray and reopen when ready. Game credentials are never used for GitHub update traffic. Retained state is outside versioned images.

Latest ZIP checksums: [SHA256SUMS.txt](SHA256SUMS.txt). Signed feed: [update.json](update.json). Trust descriptor: [update-channel.json](update-channel.json). Executables are not Windows Authenticode-signed; update signing is separate.

## Notices

This is a release-distribution repository. Dependency licenses and notices are included in the ZIPs. AION2 names/artwork belong to their respective owners; no ownership or redistribution license for third-party art is asserted. This is not an official NCSOFT application.

## Installation boundaries

Setup installs per user without silently installing drivers. Known older application versions retain settings, history and the previous image. Exit AionMarket from its tray before installing; the installer does not terminate an old portable copy. Fresh setup and default initialization do not start Steam, capture packets or enable logging. The first live connection still requires entering the game and opening/refreshing the market once. Automatic discovery and connection fixtures have passed on Windows; live first connection on ROG Ally remains unverified.
