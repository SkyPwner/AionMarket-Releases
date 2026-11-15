# AionMarket

A compact Windows market companion for AION 2 — Ludra, EU, Asmodian.

## Install and start

Download **AionMarket-Setup-1.1.1.0.exe** from [the latest release](https://github.com/SkyPwner/AionMarket-Releases/releases/latest), run it and choose Install. Exit an older AionMarket copy from its tray first. Your settings and history are retained. Python and .NET are included.

Watchlist, History, Calculator and Settings are available before entering the game. For the first connection, choose **Launch AION 2**, enter the world and open **Market once**. Connection is confirmed when real prices arrive. Open the optional price widget with **Show price widget**. The game and Steam are found automatically; any required Steam restart is explicitly confirmed first.

Wireshark with TShark and Npcap are separate first-connection prerequisites. Setup does not silently install drivers or start the game.

## Update while keeping the game open

**AION 2 can stay running while AionMarket updates.** Exit only AionMarket from its tray, install the update and reopen AionMarket. Its saved valid connection resumes automatically. Do not choose Launch AION 2 just to update the app. If an authentication session has expired or the game instance changed, reconnect explicitly.

Changelog includes version checking. Updates use a signed ECDSA-P256 feed and verified package hashes. The current app image finishes normally; its next launch uses the verified new image. Executables are not Authenticode-signed.

## Widget, history and calculator

Choose items in Watchlist. Gathering, Crafting and Amplify categories support item icons, search and rarity filters. Refresh choices are 10, 20, 30, 40, 50 or 60 seconds. The widget shows observed listed minimum prices with their real age; history shows the past 24 hours of available observations. Listed prices do not prove completed sales or continuous coverage.

Click a widget item to open its quick calculator, or use the main **Calculator** tab. Enter a sale price and quantity; optionally add a purchase price to estimate profit. The calculator assumes a 2% listing fee and a 10% sale fee, both on the listing total. Net proceeds are 88%; the separate sale credit is 90% because the listing fee was paid earlier. Estimates are shown before in-game rounding. Incoming prices never overwrite your manual input.

The rounded main window can move and minimize without staying above the game. Closing a view preserves the background session and its draft. Temporary failures retain the last prices and offer bounded recovery. Tray Exit closes AionMarket without terminating Steam or AION 2.

## Privacy and scope

Release packages contain no user settings, history, game credentials, TLS logs or captures. The first connection observes the local launch's existing traffic; the established collector then refreshes one fixed first-party summary endpoint at the selected interval. No injection, game-memory reading or automatic game input is used. History stays local. The app needs a usable game session to collect new prices.

Version 1.1.1 passed 837 native checks, 61 setup checks, exact 818-file payload verification, fresh/reinstall and TEMP upgrades from 1.1.0 and public 1.0.4, plus signed update/rollback and damaged-package refusal checks. Frozen backend files are unchanged from 1.1.0. Live 1.1 collection was observed; a live owner app-restart recovery was not performed during this release because desktop interaction was stopped. Actual ROG Ally/DPI behavior and game fee rounding remain separate acceptance checks.
