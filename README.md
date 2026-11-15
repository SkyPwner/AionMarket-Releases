# AionMarket

A compact Windows market companion for AION 2 — Ludra, EU, Asmodian.

## Install and start

Download **AionMarket-Setup-1.1.2.0.exe** from [the latest release](https://github.com/SkyPwner/AionMarket-Releases/releases/latest), run it and choose Install. Close an older AionMarket copy from its tray before a manual installer upgrade. Your settings and history are retained. Python and .NET are included.

Watchlist, History, Calculator and Settings are available before entering the game. For the first connection, choose **Launch AION 2**, enter the world and open **Market once**. Connection is confirmed when real prices arrive. Open the optional price widget with **Show price widget**. The game and Steam are found automatically; any required Steam restart is explicitly confirmed first.

Wireshark with TShark and Npcap are separate first-connection prerequisites. Setup does not silently install drivers or start the game.

## Updates

Starting with a running **1.1.2**, choose **Check for updates** or **Apply update** in Changelog. A verified update restarts AionMarket automatically. A background download waits for your Apply action. AION 2 and Steam stay running; do not choose Launch AION 2 just to update the app. The saved valid market connection resumes when the companion reopens. Expired authentication or a changed game instance requires an explicit reconnect.

An older app cannot execute the new restart code: the first transition from 1.1.1 or earlier still needs that older companion to close and reopen once. It does not require restarting the game.

Updates use a signed ECDSA-P256 feed and verified package hashes. Executables are not Authenticode-signed. If the automatic restart cannot be prepared, the existing app remains open. If the new image cannot launch after exit, reopen the stable AionMarket shortcut.

## Widget, history and calculator

Choose items in Watchlist. Gathering, Crafting and Amplify categories support item icons, search and rarity filters. Refresh choices are 10, 20, 30, 40, 50 or 60 seconds. The widget shows observed listed minimum prices with their real age; history shows the past 24 hours of available observations. Listed prices do not prove completed sales or continuous coverage.

Click a widget item for the quick calculator, or use the main **Calculator** tab. The selected item's available minimum fills the sale price automatically, including items outside the watchlist. A retained quote is labelled **Last known minimum** with its age. If no usable quote exists, enter a price. Once you edit or clear the sale price, incoming quotes preserve your draft; **Use price** explicitly replaces it.

Enter quantity and optionally a purchase price to estimate profit. The calculator assumes a 2% listing fee and a 10% sale fee, both on the listing total. Net proceeds are 88%; the separate sale credit is 90% because the listing fee was paid earlier. Estimates are shown before in-game rounding.

The rounded main window can move and minimize without staying above the game. Closing a view preserves the background session and its draft. Temporary failures retain the last prices and offer bounded recovery. Tray Exit closes AionMarket without terminating Steam or AION 2.

## Privacy and scope

Release packages contain no user settings, history, game credentials, TLS logs or captures. The first connection observes the local launch's existing traffic; the established collector then refreshes one fixed first-party summary endpoint at the selected interval. No injection, game-memory reading or automatic game input is used. History stays local. The app needs a usable game session to collect new prices.

Version 1.1.2 passed 964 native checks, 548 market Python tests, 61 setup checks and exact 819-file payload verification. Hidden tests against the final assembly and a retained market frame verify decimal wire prices, calculator defaults and preserved timestamps. The calculator adds no market request. Update restart fixtures use harmless child processes; actual ROG Ally/DPI behavior and game fee rounding remain separate acceptance checks.
