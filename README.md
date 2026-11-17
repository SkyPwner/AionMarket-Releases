# AionMarket

A compact Windows market companion for AION 2 — Ludra, EU, Asmodian.

## Install

Download **AionMarket-Setup-1.2.13.0.exe** from [the latest release](https://github.com/SkyPwner/AionMarket-Releases/releases/latest) and choose Install. Python and .NET are included. Your watchlist, settings and recorded history are retained.

Choose **Launch AION 2**, enter the world and open **Market once**. A valid existing connection can resume when only AionMarket is updated. Wireshark with TShark and Npcap are separate first-connection prerequisites; Setup does not install drivers or launch the game.

## Use

- **Alt+Z** opens the main window. Change or disable it in **Settings → Open main window**.
- Search and filter by category and coloured rarity. Sort by price or estimated profit.
- The optional widget shows item icons, prices and age; controls appear on hover.
- Click an item for the calculator. Purchase edits keep an untouched sale field at a target of at least 1,000 estimated profit per unit after the 2% listing and 10% sale fees.
- **Helper** checks gathering, crafting and amplify items. It compares buying the first one to four complete lots and reselling below the next offer. Buy total, Sell each, You need and estimated Profit show the plan. Only fresh, supported estimates meeting the profit threshold appear. It scans while the tab is open and never buys or sells for you.
- Selected-item **Offers average** is the quantity-weighted average of observed current listings. **Below your sale** counts observed offers strictly cheaper than your entered unit sale price. Coverage may be partial and pages can change during a read.
- The separate `~price` on item cards is the 24-hour average of recorded minimum listing prices. History contains observations, not completed sales.

Estimates and price gaps do not guarantee a sale or profit. Prices are recorded while the app and a valid game session are running; no missing full-day history is created later. Scan duration depends on the server, network and supported items.

## Update

Choose **Check for updates → Apply update**. AionMarket closes its previous instance and starts the new version. Only the companion needs to restart; keep AION 2 running. The updater verifies the signed feed and package hash before activation. An expired or different game session still needs a fresh connection.

If an old companion cannot finish closing, exit AionMarket and retry the latest installer. Settings/history remain retained. Windows SmartScreen may prompt because the binaries are not Authenticode signed; feed signing is a separate update-integrity check.

## Support

Steam/game locations are detected automatically; Settings can select executables if discovery fails. Restricted game verification may require running AionMarket with the same permissions as the game. **Open logs** and **Create support report** are in Settings; do not share private capture or key files.

Windows 11 x64 is the target. Local tests do not replace acceptance on another device.
