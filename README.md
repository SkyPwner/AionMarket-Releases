# AionMarket



A compact Windows market companion for AION 2 — Ludra, EU, Asmodian.



## Install and start



Download **AionMarket-Setup-1.1.9.0.exe** from [the latest release](https://github.com/SkyPwner/AionMarket-Releases/releases/latest), run it and choose Install. Setup closes a supported older AionMarket copy and opens the installed version automatically. Your settings and history are retained. Python and .NET are included.



Watchlist, History, Calculator and Settings are available before entering the game. For the first connection, choose **Launch AION 2**, enter the world and open **Market once**. Connection is confirmed when real prices arrive. Open the optional price widget with **Show price widget**. The game and Steam are found automatically; any required Steam restart is explicitly confirmed first.



Wireshark with TShark and Npcap are separate first-connection prerequisites. Setup does not silently install drivers or start the game.



## Game locations



Detection is automatic. If Steam or AION 2 cannot be identified, open **Settings → Game locations** and use **Browse** to choose the installed `steam.exe` and, if needed, `AION2.exe` or `AION2-Win64-Shipping.exe`. Choose **Automatic** to clear an override. Save changes, then choose **Launch AION 2** and open Market once. Selecting or saving a file does not launch the game.



Locations are saved separately on each Windows account. No process ID is saved. Secondary/SD libraries and Unicode paths are supported. A missing or moved selection can be replaced without losing history. Only one actual game client may be running while establishing a fresh connection. An existing valid saved connection still belongs to its original game instance.



## Updates



Starting with a running **1.1.2**, choose **Check for updates** or **Apply update** in Changelog. A verified update restarts AionMarket automatically. A background download waits for your Apply action and leaves the running version active until then. AION 2 and Steam stay running; do not choose Launch AION 2 just to update the app. The saved valid market connection resumes when the companion reopens. Expired authentication or a changed game instance requires an explicit reconnect.



Version 1.1.8 also checks which copy owns the tray. Starting a newer copy replaces an older supported instance instead of silently showing it. Setup supports the first transition from the released 1.1.5 and 1.1.6 companions without a manual tray Exit.



Updates use a signed ECDSA-P256 feed and verified package hashes. Executables are not Authenticode-signed. If the automatic restart cannot be prepared, the existing app remains open. If the new image cannot launch after exit, reopen the stable AionMarket shortcut.



Version 1.1.9 restores a failed price display automatically, keeps calculator quote ages accurate, and enables an explicit retry after a local 60-second rate-limit wait. Settings stay editable if saving fails. Installed-tool checks, session binding and private temporary files are hardened.

## Widget, history and calculator



Choose items in Watchlist. Gathering, Crafting and Amplify categories support item icons, search and rarity filters. Refresh choices are 10, 20, 30, 40, 50 or 60 seconds. The widget shows observed listed minimum prices with their real age; history shows the past 24 hours of available observations. Listed prices do not prove completed sales or continuous coverage.



Click a widget item for the quick calculator, or use the main **Calculator** tab. The selected item's usable minimum fills **Bought for** once. **Sale price** defaults to the lowest whole-unit price that yields at least **+1,000 profit per item** after both fees. For a cost of 18,880, the suggested sale is 22,591 and estimated profit is 1,000.08 per item. Quantity scales the totals.



Market updates preserve your purchase cost and manual edits, including cleared fields. **Use as cost** explicitly takes the latest available minimum and restores the automatic sale suggestion. A retained quote is labelled **Last known minimum** with its age; unavailable quotes do not overwrite your calculation.



The calculator assumes a 2% listing fee and a 10% sale fee, both on the listing total. Net proceeds are 88%; the separate sale credit is 90% because the listing fee was paid earlier. Estimates are shown before in-game rounding. A suggested price is a calculation, not a promise that an item will sell at that price.



The rounded main window can move and minimize without staying above the game. Closing a view preserves the background session and its draft. Temporary failures retain the last prices and offer bounded recovery. Tray Exit closes AionMarket without terminating Steam or AION 2.



## Running-game compatibility



Version 1.1.6 adds a second documented Windows image-name format when the usual query fails. It keeps the same limited-information process handle and the existing game-instance checks. If a game file was selected manually, its full path must still match. Support reports show which query succeeded and the safe numeric failure codes. This addresses the observed blocked check; a report from the affected device is still needed to confirm recovery.



## Help with a connection problem



Open **Settings → Support → Create diagnostic report**, then **Open logs folder**. Share the newest `support-…json` file. Reports stay on your PC until you choose to share them; nothing uploads automatically. The report distinguishes installation discovery, running-game detection and metadata access failures. It includes app/Windows versions and safe connection status, without account credentials, session keys, packet content, raw errors, usernames or full paths.



Safe event logs are stored beside the reports. Each app instance writes at most four 64 KiB event chunks; earlier sessions and reports are retained. Support actions do not save an unfinished settings draft or launch/restart the game.



## Privacy and scope



Release packages contain no user settings, history, game credentials, TLS logs or captures. The first connection observes the local launch's existing traffic; the established collector then refreshes one fixed first-party summary endpoint at the selected interval. No injection, game-memory reading or automatic game input is used. History stays local. The app needs a usable game session to collect new prices.



Version 1.1.9 passed 575 market Python tests, 1210 native checks, 240 update-core checks, 97 Setup checks and exact 822-file payload verification. Further fixtures cover 39 installer process-lifetime cases, actual 1.1.8/1.1.9 settings and updater consumers, and real harmless handoff. Installation on the owner’s PC replaced 1.1.8 and resumed price collection while preserving history and the running game/Steam. Physical ROG Ally behavior and in-game fee rounding remain separate acceptance checks.


## How prices are obtained

The first connection uses local TLS key logging and a short network capture. Subsequent updates send fixed read-only market requests using the prepared session. This is not passive-only monitoring. Before enabling logging, the app explains local key storage and inheritance by supporting Steam child processes. Logging may continue after AionMarket closes; fully exit Steam and start Steam normally to stop it. Updating the companion does not require restarting the game.
