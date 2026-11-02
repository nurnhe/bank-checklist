# Bank Checklist

A small checklist for opening a business bank account: general steps you do once, a list of banks you're comparing, the documents each bank asks for, and steps that only apply at one bank.

**Use it as a phone app:** open the GitHub Pages address in Chrome on Android, then tap ⋮ → **Install app** (or **Add to Home screen**). It opens full screen with its own icon and works offline.

## Files

- `bank-checklist.html` is the page itself. The same file is published as a Claude artifact.
- `build.py` wraps it into `index.html` with the app manifest and offline support. Run `python3 build.py` after editing `bank-checklist.html`.
- `manifest.webmanifest`, `sw.js` and `icons/` make it installable and work offline. Bump the cache name in `sw.js` on every change.

## Features

- **Russian and Serbian:** everything, including the starting list, switches between Russian and Serbian (Latin) with the RU / SR buttons. The choice is saved on the device. Steps and documents you type or edit stay as you wrote them.
- **One page, no tabs:** a "For every bank" card at the top with general steps and general documents, then one collapsible section per bank. Each bank has its status (Considering, Applying, Account open, Not for me), its own documents, its own steps, notes, and its name and Delete under a fold. The closed header shows the status and document and step counts. Tick, add, edit, reorder or delete anything.
- **Document steps:** every document (general or in a bank) has its own small checklist, for example "Submitted the request", "Received the document". Once all of a document's steps are ticked, the document counts as received; a document without steps is ticked by hand.
- **Starting list:** no general steps. Two general documents, the APR extract and the residence certificate from MUP (uverenje o boravku), each with "Submit the request" and "Receive the document" steps. Everything can be edited or deleted. No banks until you add them.
- **Backup:** save a backup file or restore from one at the bottom of the page.
- **Colour scheme:** Auto, Light or Dark, saved under `nurnhe-theme`, the setting shared with the other apps on nurnhe.github.io.
- **Look:** its own "ledger" design: warm paper with a dot grid, white cards, cobalt for actions, green for done. Fonts are Unbounded and Onest, which cover Cyrillic and Latin.

## Data

When the page runs as a Claude artifact, data is saved in the artifact's database and syncs across devices. Anywhere else, including the installed app, it saves to the browser's `localStorage` on that device.

## Credits

- Tab icons: [Tabler Icons](https://github.com/tabler/tabler-icons) (MIT License)
- Fonts: Unbounded and Onest, from Google Fonts (SIL Open Font License)
