# Desktop App

The desktop app for Mac and Windows shows your team in its own window. It behaves like a regular program: its own menu bar, keyboard shortcuts, and it remembers the window position. It can also fetch the patch directly from an Eos console.

## Installation

- **Windows:** [Microsoft Store](https://apps.microsoft.com/detail/9n4d59hvlwn0?hl=en-US). Updates install automatically.
- **Mac:** [Download the latest version](https://github.com/Plobli/luxstage-desktop/releases/latest) (file `…-arm64.dmg`, for Macs with Apple silicon). The app is signed, checked by Apple and updates itself.

On first launch, enter your team name, for example `my-theater` for `my-theater.luxstage.app`. Use **Switch team …** in the menu to change teams later. You can create a new team right on the start page.

## Menu bar

Import, export, history, find, undo and redo are in the menu bar. That is why these buttons no longer appear in the show header.

| Menu | Command | Mac | Windows |
|------|---------|-----|---------|
| File (Windows: Show) | Import … | ⌘I | Ctrl+I |
| | Export as PDF … | ⇧⌘E | Ctrl+Shift+E |
| | Export as CSV | | |
| | Show history | ⌘Y | Ctrl+H |
| Edit | Undo | ⌘Z | Ctrl+Z |
| | Redo | ⇧⌘Z | Ctrl+Y |
| | Find … | ⌘F | Ctrl+F |
| Navigation | Back / Forward | ⌘[ / ⌘] | Ctrl+[ / Ctrl+] |

In text fields, undo and redo apply to the typed text, otherwise to the show. Open settings with ⌘, (Mac) or Ctrl+, (Windows). The menu items are named in German.

## Toolbar

Undo/redo, filter and search sit at the top of the header next to the show name. On the Mac the header doubles as the title bar, so you can drag the window there. Search works in the channel list, towers, fly system, locations and photos. In other views it is greyed out.

## Console sync with Eos

The desktop app fetches the patch straight from the console. New channels, addresses and devices land in the channel list without an export file. You choose whether to add new items only, merge, or mirror the console. Details: [Import from EOS](/en/webapp/import-eos).
