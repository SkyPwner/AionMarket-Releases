# AionMarket

A compact Windows market companion for AION 2 — Ludra, EU, Asmodian.

## Install

Download **AionMarket-Setup-1.2.5.0.exe** from [the latest release](https://github.com/SkyPwner/AionMarket-Releases/releases/latest), run it and choose Install. Python and .NET are included. Your watchlist, settings and recorded history are retained.

Choose **Launch AION 2** in the app, enter the world and open **Market once**. A previously valid connection can resume without restarting the game when only AionMarket is updated. Wireshark with TShark and Npcap are separate first-connection prerequisites; Setup does not install drivers or launch the game.

## Prices and calculator

- Search, category and rarity filters, real item icons and numeric price sorting.
- A small optional widget: item icon, price and source age; controls appear on hover.
- Click a widget item to open its profit calculator. The current minimum seeds purchase cost; an untouched sale field follows a target of at least 1,000 profit per unit after the configured 2% listing and 10% sale fees.
- **Offers average** loads current offers for the selected item in the background. It is a quantity-weighted unit average. **Below your sale** counts offers strictly cheaper than your entered sale price, including an offer you might buy.
- `partial` means incomplete coverage; its count is a lower bound. Offers can change while being read. A mean or price gap does not establish a completed sale or guarantee profit.
- The separate `~price` on item cards is the 24-hour average of recorded minimum listing prices. History contains locally observed listings, not completed sales.

Prices are recorded while the companion and a valid game session are running. Closing the app does not create a full-day history later.

## Update

Use **Check for updates**, then **Apply update**. Only the companion needs to restart; do not choose Launch AION 2 just to apply an app update. A background download waits for Apply. The updater verifies the signed feed and package hash before activation.

If an update cannot finish or an old version remains, exit AionMarket and run the latest installer again. A local Setup transition required a retry; it preserved settings and history. Game authentication that expired or belongs to a different game instance requires a fresh connection.

## Troubleshooting

Steam/game locations are detected automatically. Use Settings to choose installed executables if detection fails. If game verification fails because access is restricted, run AionMarket with the same permissions as the game. Settings includes **Open logs** and **Create support report**; do not share private capture or key files.

Windows 11 x64 is the release target. This release has local Windows validation; separate ROG and display acceptance remains with the owner.
