# Focus (iOS)

The **Focus** tab is the central focusing view of the show. It displays all channels of the production in a list sorted by placement: **towers** first (by slot), then **locations**, then **fly system** (by position on the bar), and finally unplaced channels, grouped by **position** (e.g. "FOH SL Slot"). You set view and sorting in the [filter](#filter-and-view); sorting also with **Sort by number** in [Settings](./settings#channel-list).

## Channel display

<img src="/img/ios/einleuchten-kanalliste.png" alt="Channel list" class="ios-screenshot">

Each channel is displayed as a card with the following elements:

| Element | Meaning |
|---------|---------|
| **Large channel number** (e.g. `001`) | Turns red once the channel is marked as focused |
| **Name and fixture** | e.g. "Person Stage Left · 1/1 · ETC Source Four 26°" |
| **Focus circle** (bottom left, below the number) | Tap → mark channel as focused (red checkmark) |
| **OSC toggle** (bottom right) | Switch channel to Full via OSC; active = green toggle, card highlighted in pink |

## Filter and view

The **filter** (icon next to the progress) holds all list settings:

- **Show:** **With lighting note**, **Groups** (only if there are groups) or **All**.
- **Sort by placement:** on (default) sorts by setup, off by stage position and number.
- **Priority** and **tags**.

The number on the filter shows how many filters are active. "Groups" or "All" counts too. **Reset** sets the view back to "With lighting note" and clears priority and tag filters. With "All", the **+** for adding a channel appears next to the filter. The dot in the **Console** button at the bottom right shows whether the console is connected.

At the top right next to the show title you switch between **list** and **grid**.

## Grid view

In the grid view each channel is a tile with its number. A green border means checked, an orange fill means the light is on at the console. Tap a tile to open the channel card with note, photos, checkmark and light switch. Long-press to edit the channel.

### Several channels at once

This is how you focus several fixtures together:

1. **Select:** Swipe horizontally across the tiles. All tiles between start and finger are selected, across several rows too. If you start on a tile that is already selected, you deselect. Swiping vertically scrolls as usual. Alternatively, tap the **check circle** at the top and then tap single tiles. Selected tiles have a coloured border and a checkmark.
2. **On:** A bar appears at the bottom. **On** switches all selected channels on at the console, **Off** switches them off again. Selecting alone does not switch any light.
3. Focus the fixtures.
4. **Check:** Checks all selected channels, switches their light off and ends the selection. If all are already checked, the button reads **Uncheck**.

The **number** on the left of the bar shows how many channels are selected. Tap it to show only the selected tiles, tap again to show all. The filled check circle at the top ends the selection.

With two or more channels on, the orange light button with **Check** and **All off** also appears in the grid view.

## Where is the channel?

Below each channel, **pills** show where it is set up, e.g. "Tower 1 · Slot 3", a batten of the overhead machinery or a location. Channels without a place show no pill. Pills appear in the list and in the tile sheet.

Tapping a pill opens a **quick look** without switching tabs: for a tower you see all slots with channel numbers, for a batten all fixtures by position, for a location all its channels. Your channel is highlighted. **Edit** opens the entry for changes.

## Progress

The status in the top right shows how many channels have already been focused, e.g. `64 · 50%`.

### Hints

Channels whose note you marked as a **hint** in the web app (for example "turn away") are not fixtures to focus. They appear as a slim orange row without an on/off switch. Consecutive hints with the same text form one row, e.g. "136–147 · 12". One tap checks them all. They do not count towards progress. A separate count with a flag sits next to it, e.g. `⚑ 0/1`.

## Groups

If you created circuit groups in the web app, the list shows one card per group with name, circuit range and counter. A circuit is listed under the first group it belongs to; other groups show as small chips.

- Tap the **box in the group header** to check all circuits of the group (tap again to clear them). The box shows "partial" when only some are done. Single circuits can always be checked on their own.
- Tap the **title or arrow** to collapse or expand the group.
- The **chip bar** above the list: tap a chip to filter the list to that group, tap again to clear the filter.

## Search

**Search** in the bottom bar opens a sheet over the current view and searches channels, notes and plans of the show. A result jumps to the right place; the X or a swipe down takes you back to where you were.

## Workflow: focusing fixtures

1. Find the channel in the list by searching or scrolling
2. Switch **toggle** on → the app sends @ Full to the EOS console (card is highlighted in colour)

<img src="/img/ios/einleuchten-osc-toggle.png" alt="OSC toggle active" class="ios-screenshot">

3. Physically focus the fixture
4. Tap **checkmark** → channel is marked as done (red checkmark, number turns red) and the fixture is switched off via the EOS console. Alternatively, without marking the fixture as done: switch toggle off

<img src="/img/ios/einleuchten-fokussiert.png" alt="Channel focused" class="ios-screenshot">

<img src="/img/ios/einleuchten-alle-fokussiert.png" alt="All channels focused" class="ios-screenshot">

5. → continue to the next channel

::: tip Photos during focusing
**Photos** assigned to the channel are directly accessible in the list — ideal for comparing the focus position.
:::

## Editing

The tab is now called **Channel list**. In the [filter](#filter-and-view) you choose whether only channels with a lighting note, the groups or all channels appear. Long-press a channel to edit it. See [Editing in the apps](./editing).
