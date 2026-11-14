# AionMarket

A compact Windows price widget for AION 2 — Ludra, EU, Asmodian.

## Install and start

Download **AionMarket-Setup-1.0.4.0.exe** from [the latest release](https://github.com/SkyPwner/AionMarket-Releases/releases/latest), run it and choose Install. Exit an older AionMarket copy from its tray first. Your settings and history are retained. Python and .NET are included.

Choose **Launch AION 2** in the app, enter the world and open **Market once**. AionMarket waits in the background and opens the widget when prices arrive. No separate Connect button or short countdown. The game and Steam are detected automatically; if Steam must restart, the app asks first because running Steam games may close.

Wireshark with TShark and Npcap are separate first-connection prerequisites. The app checks them and links the official download when needed. Setup does not silently install drivers or start the game.

## Widget and history

Choose items in Watchlist. Gathering, Crafting and Amplify Stone categories support item icons, search and rarity filters. Set refresh to10,20,30,40,50 or60seconds. The widget shows the latest observed listed minimum and its age; older observations keep their actual age. History shows the past24hours of observed prices with rounded Low/Average/High cards and a chart. Listed prices do not prove completed sales or continuous coverage.

The rounded main window has Watchlist, History, Settings and Changelog. Ordinary windows can move and minimize without staying above the game. A minimized connection continues waiting; closing it cancels its own connection attempt. Tray Exit closes AionMarket without terminating Steam or the game.

## Updates and privacy

Changelog includes version checking. Updates use a signed ECDSA-P256 feed and verified package hashes. Executables are not Authenticode-signed. Release packages contain no user settings, history, game credentials, TLS logs or packet captures.

Passive first connection observes the local launch's existing traffic, then the established collector refreshes the fixed first-party summary endpoint at the selected interval. No injection, game-memory reading, or input automation is used. Retained history is local. The app must run with a usable game session to gather new observations.

## Verified scope

Windows x64 fixtures, exact packaged startup checks, fresh/reinstall and public3-to4 TEMP upgrade, signed update/rollback and damaged-package refusal were checked. The repaired live game connection, cold ExitLag timing and actual ROG Ally usability remain owner-controlled acceptance work. Synthetic layout tests are not actual handheld/DPI acceptance.
