# Development log

What is being built for the helper, newest first. Feature names match the app's own pages. Nothing in this log changes your install; updates arrive through the app's Updates button as always. The current public version stays 2.36.0 until testing completes.

## 2026-08-18 (evening)

**Done and tested on the development branch (not yet released):**

- Pick the arm and disarm hotkey in Setup: a chooser now offers F1 to F12 and Insert, Delete, Home, End, Page Up and Page Down, all keys with no ordinary typing meaning. The hotkey already worked while the game has focus; this lets you move it off F8 if something else needs that key.
- New installs now start with the safety settings already on: the staff watch and leaving a shard when a boss shows up. Your existing settings are untouched; this only changes what a fresh setup begins with.
- Keep the session alive (settings in place, the relaunch itself still in testing): three switches under Setup to restart the game and log back in when an overnight session stops, if the client closes or crashes, if it stops responding, or if it stops getting kills, gold and exp for a set number of minutes. At most two restarts in any thirty minutes so a broken session cannot loop.

## 2026-08-18 (afternoon)

**Done and tested on the development branch (not yet released):**

- This map: the Loot page's catalog gains an All / This map switch. This map lists every drop the monsters on your current map can produce, read live from your running session, so you can set rules for exactly what you are farming. The selected item's header also says when it drops on your current map.
- The full item catalog: with a session running, the app now learns the game's whole item list, including grimoires and cosmetics, and keeps it for offline editing too. The catalog pane says when the live catalog is merged in.
- Item icons: every catalog row and the selected item header now show the item's own art.

## 2026-08-18

**Done and tested on the development branch (not yet released):**

- The Loot page rebuilt as a full editor: an item catalog with search and a category filter in your bag tab order, a rule pane where one click sets an item to Ignore, Favorite, Dismantle or Storage, and an active rules pane showing your category defaults and your exceptions at a glance.
- Category defaults: set one rule for a whole category at once (Equipment, Mats, Gems, Consumables and the rest) and every item in that category follows it. An item rule always wins over its category default, and setting an item to Ignore shields it from the default.
- Export and import: copy your whole loot setup, save it to a file, and load it back on another PC or from a friend.
- Storage fix: an item the game quietly refuses to bank no longer wedges the deposits; after a few refused rounds it is set aside out loud and the batch moves on.

## 2026-08-17

**Done and tested on the development branch (not yet released):**

- A new look for the whole app: a left navigation rail with ten pages (Dashboard, Combat, Targets, Farm, Loot, Setup, Sentry, Logs, Licence, Guide), a palette drawn from the guild emblem, a persistent live status strip in the header, and a larger default window.
- Loot rules editor, first version, on the Loot page: edit the rules the loot automation runs, with saves reaching a running session within seconds.
- Farm page: warp to town at low health, automatic return to your farm map afterwards, death handling, and channel automation (timed rotation, empty map hop, preferred channel lock).
- A town sell trip: when bag weight passes your threshold the bot visits the material vendor and sells by your rules, with a hard guard that refuses the whole trip if any favorited item could be sold by mistake.
- Sentry page: an optional watch that pauses the bot for a set number of minutes when certain other players are rendered nearby. Off by default.
- All three combat movement styles on the Combat page, each off by default and each meant to be proven in Dry run before trusting: orbit the target while attacking, prioritize monster packs, and pack kite (gather monsters into one pack, then fight them together). The three are mutually exclusive; ticking pack kite turns the other two off.
- The orbit polish fixes from an internal review: corrected steering when several monsters are on you, extra stand aside guards, and a write verification counter on the session summary.

**In progress, not yet complete:**

- Reliability features: automatic recovery from a stuck loading screen, anti AFK, party and trade popup handling, cast retry.
- A launch mode for running the game with a different plugin setup without uninstalling anything.
- A live target list and a vitals strip in the header.

Release date undecided. Everything above lives on a development branch and ships only after live testing.
