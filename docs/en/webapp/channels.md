# Channels

The **Channels** tab (labelled **"Channel list"** in the app sidebar) is the main view of a show and displays the complete channel plan.

::: tip Inline help in the app
Next to the column headers of the channel table and in the Setup area, small help icons show brief explanations for each field directly in the app.
:::

## Live collaboration (presence)

Once at least one person is connected to a show, small avatars (initials) for each signed-in person appear at the top of the show bar. Purely informational, not a lock.

- Hovering shows a tooltip with the name and connected devices (e.g. "ios, web")

Who may write is governed separately by the edit lock, not by the presence display. Other users' changes appear in real time, without reloading the page.

## Edit lock and takeover

While one person is editing the show, it is locked for everyone else: a badge reads "Being edited by {person}", and editing is blocked.

Other users can request a takeover:

- The requester sees "Takeover requested — waiting for release"
- The current editor sees a "Takeover requested" dialog with the options **"Release"** and **"Ignore"**
- If the current editor doesn't respond, a countdown starts ("Takeover forceable in Xs"); afterwards the requester can force the takeover via **"Take over now"**

## Save conflicts

If two people (e.g. via parallel sessions or an expired lock) edit the same channel list or section at the same time, saving triggers the **"Someone else has saved"** dialog: while you were editing, another person already saved, so your changes haven't been applied yet. The options are:

- **"Use other version"** – discards your changes and loads the saved version
- **"Overwrite anyway"** – overwrites the saved version with your changes

## Channel plan structure

The table has the following columns:

| Column | Meaning |
|--------|---------|
| **Chan** | Channel number, plain integer, e.g. "1" |
| **DMX** | Universe/address, e.g. "1/121" |
| **Color** | Colour filter (gel code), e.g. "L201/R371" or "RGB", "variable" |
| **Qty.** | Number of identical fixtures at this position |
| **Device** | Fixture name, e.g. "ETC Source Four 26°" |
| **Notes** | Free-text note, e.g. "Key light stage left, narrow spot" |
| **Assign** | Button to assign an installation spot (see below) |

Channels are grouped by **positions** (e.g. "FOH BAR LEFT", "OVERHEAD BAR 1", "SIDE BOOM SL"). The number of channels per position is shown as a number to the right of the position name.

## Select and edit a channel

1. Click on a row – a **drag handle** (⠿) appears on the left, an **×** button on the right
2. Edit fields directly:

| Field | Action |
|-------|--------|
| **Channel number (left)** | Click → enter number |
| **Dimmer address (right)** | Click → enter address |
| **Colour** | Click → dropdown with available gel codes appears (e.g. "L201 / R371 Full C.T. Blue"). Also selectable: **"No Color"** (no filter) or **"Custom"** for free-text entries (e.g. "R02" or "warm white") |
| **Fixture** | Click → enter fixture name |
| **Notes** | Click → enter free text |

::: details DMX address is normalized automatically
When you leave the address field, the input is automatically formatted as "universe/address" — e.g. "129" becomes "1/129" and "1/1" becomes "1/001". Plain numbers above 512 are treated as a continuous address spanning multiple universes (e.g. "515" → "2/003").
:::

## Toggle channel status

The **channel number** appears in three colours:

- **White** – no note and no installation spot
- **Green** – note present, or assigned to an installation spot (lighting rig slot or bar)
- **Yellow** – active in the show (e.g. after an EOS import), but neither a note nor an installation spot is set yet

The same legend is also available as inline help (help icon) next to the channel table in the app.

## Add a channel

Below each position there is a **"+ Add channel"** button. Clicking it adds a new empty channel to that position.

## Delete or clear a channel

Click the channel (to activate it), then click the **×** icon on the right of the row. A dialog offers two options:

- **Clear channel** – removes only the note and colour, the row remains
- **Delete row** – removes the channel entirely

## Assign a channel to an installation spot

Hovering over a channel row reveals the **"Assign"** button on the right (before the delete button), with three options:

- **Place in floor plan** – opens the [Floor Plan](./floor-plan) and places the channel there
- **Assign lighting rig slot** – opens [Setup — Lighting Rigs](./setup-gestelle) to assign it to a rig
- **Assign bar** – opens [Setup — Bars](./setup-zugstangen) to place it on a bar

If the channel is already assigned to a rig slot or a bar, the installation spot is additionally shown as a small badge below the note.

::: tip Duplicate warning
Assigning the same DMX address or channel number twice triggers a warning: "Duplicate DMX address!" or "Duplicate channel number!".
:::

## Change order (drag & drop)

Use **drag & drop** on the ⠿ handle on the left to reorder channels within a position.

## Rename a position

When hovering over a position heading, the **"Rename position"** button appears – click it and enter a new name.

## Search

In the search field at the top right (**"Search channels …"**) channels, fixtures or notes can be filtered in real time.

## Completeness check

Next to the channel table, a badge shows whether the show is complete:

- **Green checkmark** – all channels fully filled in
- **Yellow warning icon with a number** – number of channels with missing information

Clicking the badge opens a breakdown by missing field (no fixture, no position, no address). Clicking a row filters the channel table to exactly those channels; an **×** next to the active filter clears it.

## Keyboard shortcuts

| Action | Shortcut |
|--------|----------|
| Undo | ⌘Z (Mac) / Ctrl+Z (Win) |
| Redo | ⌘⇧Z (Mac) / Ctrl+Y (Win) |
