# Bank Checklist

A small checklist for opening a business bank account: general steps you do once, a list of banks you're comparing, the documents each bank asks for, and steps that only apply at one bank.

**Use it as a phone app:** open the GitHub Pages address in Chrome on Android, then tap ⋮ → **Install app** (or **Add to Home screen**). It opens full screen with its own icon and works offline.

## Files

- `bank-checklist.html` is the page itself. The same file is published as a Claude artifact.
- `build.py` wraps it into `index.html` with the app manifest and offline support. Run `python3 build.py` after editing `bank-checklist.html`.
- `manifest.webmanifest`, `sw.js` and `icons/` make it installable and work offline. Bump the cache name in `sw.js` on every change.

## Features

- **Russian and Serbian:** everything, including the starting list, switches between Russian and Serbian (Latin) with the RU / SR buttons. The choice is saved on the device. Steps and documents you type or edit stay as you wrote them.
- **One page (Чек-лист / Lista):** general steps for every bank at the top, then one collapsible section per bank. Tick, add, edit, reorder or delete any step. A bank's section has its status (Considering, Applying, Account open, Not for me), the documents it asks for (pick from your list or add new), its own steps, notes, and its name and Delete under a fold. The closed header shows the status and document and step counts.
- **Documents:** one shared list of your papers. Tick a document once you have it and it counts as ready for every bank that asks for it. Each document shows which banks need it.
- **Starting list:** no general steps (you write your own). Seven typical documents for a Serbian business account (APR extract, PIB, founding act, director's ID, beneficial owners, residence permit, stamp), all editable. No banks until you add them.
- **Backup:** save a backup file or restore from one at the bottom of the Documents tab.
- **Colour scheme:** Auto, Light or Dark, saved under `nurnhe-theme`, the setting shared with the other apps on nurnhe.github.io.
- **Look:** its own "ledger" design: warm paper with a dot grid, white cards, cobalt for actions, green for done. Fonts are Unbounded and Onest, which cover Cyrillic and Latin.

## Data

When the page runs as a Claude artifact, data is saved in the artifact's database and syncs across devices. Anywhere else, including the installed app, it saves to the browser's `localStorage` on that device.

## Credits

- Tab icons: [Tabler Icons](https://github.com/tabler/tabler-icons) (MIT License)
- Fonts: Unbounded and Onest, from Google Fonts (SIL Open Font License)
