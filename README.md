# Bank Checklist

A small checklist for opening a business bank account: general steps you do once, a list of banks you're comparing, the documents each bank asks for, and steps that only apply at one bank.

**Use it as a phone app:** open the GitHub Pages address in Chrome on Android, then tap ⋮ → **Install app** (or **Add to Home screen**). It opens full screen with its own icon and works offline.

## Files

- `bank-checklist.html` is the page itself. The same file is published as a Claude artifact.
- `build.py` wraps it into `index.html` with the app manifest and offline support. Run `python3 build.py` after editing `bank-checklist.html`.
- `manifest.webmanifest`, `sw.js` and `icons/` make it installable and work offline. Bump the cache name in `sw.js` on every change.

## Features

- **Russian and Serbian:** everything, including the starting list, switches between Russian and Serbian (Latin) with the RU / SR buttons. The choice is saved on the device. Steps and documents you type or edit stay as you wrote them.
- **Steps:** general steps for every bank, numbered, with notes. Tick them off, add new ones, and edit, reorder or delete any step. A progress card on top counts general steps and documents.
- **Banks:** add each bank you're looking at. Each card shows its status (Considering, Applying, Account open, Not for me) and progress bars for its documents and its own steps. Open a bank to edit its name and notes, choose the documents it asks for, add new documents, and add steps that only apply there.
- **Documents:** one shared list of your papers. Tick a document once you have it and it counts as ready for every bank that asks for it. Each document shows which banks need it.
- **Starting list for Serbia:** for a company that is already registered. Seven steps (compare banks, who signs, stamp, appointment, signing, e-banking and card, account number to the accountant) and seven documents (APR extract, PIB, founding act, director's ID, beneficial owners, residence permit, stamp). Everything can be edited or deleted. There are no banks until you add them.
- **Backup:** save a backup file or restore from one on the Steps tab.
- **Colour scheme:** Auto, Light or Dark, saved under `nurnhe-theme`, the setting shared with the other apps on nurnhe.github.io.
- **Look:** its own "ledger" design: warm paper with a dot grid, white cards, cobalt for actions, green for done. Fonts are Unbounded and Onest, which cover Cyrillic and Latin.

## Data

When the page runs as a Claude artifact, data is saved in the artifact's database and syncs across devices. Anywhere else, including the installed app, it saves to the browser's `localStorage` on that device.

## Credits

- Tab icons: [Tabler Icons](https://github.com/tabler/tabler-icons) (MIT License)
- Fonts: Unbounded and Onest, from Google Fonts (SIL Open Font License)
