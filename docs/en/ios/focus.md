# Focus (iOS)

The **Focus** tab is the central focusing view of the show. It displays all channels of the production in a list sorted by placement: **towers** first (by slot), then **locations**, then **fly system** (by position on the bar), and finally unplaced channels, grouped by **position** (e.g. "FOH SL Slot"). The **stack icon** in the channel list switches to sorting by stage position and number, as does **Sort by number** in [Settings](./settings#channel-list).

## Channel display

<img src="/img/ios/einleuchten-kanalliste.png" alt="Channel list" class="ios-screenshot">

Each channel is displayed as a card with the following elements:

| Element | Meaning |
|---------|---------|
| **Large channel number** (e.g. `001`) | Turns red once the channel is marked as focused |
| **Name and fixture** | e.g. "Person Stage Left · 1/1 · ETC Source Four 26°" |
| **Focus circle** (left) | Tap → mark channel as focused (red checkmark) |
| **OSC toggle** (right) | Switch channel to Full via OSC; active = green toggle, card highlighted in pink |

## Where is the channel?

Below each channel, **pills** show where it is set up, e.g. "Tower 1 · Slot 3", a batten of the overhead machinery or a location. Channels without a place show no pill. Pills appear in the list and in the tile sheet.

Tapping a pill opens a **quick look** without switching tabs: for a tower you see all slots with channel numbers, for a batten all fixtures by position, for a location all its channels. Your channel is highlighted. **Edit** opens the entry for changes.

## Progress

The status in the top right shows how many channels have already been focused, e.g. `64 · 50%`.

## Groups

If you created circuit groups in the web app, the list shows one card per group with name, circuit range and counter. A circuit is listed under the first group it belongs to; other groups show as small chips.

- Tap the **box in the group header** to check all circuits of the group (tap again to clear them). The box shows "partial" when only some are done. Single circuits can always be checked on their own.
- Tap the **title or arrow** to collapse or expand the group.
- The **chip bar** above the list: tap a chip to filter the list to that group, tap again to clear the filter.

## Search

The search field at the top filters the channel list in real time by name, fixture or note.

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

The tab is now called **Channel list**. The **With note / All** switch shows only channels with a note, or all channels. Long-press a channel to edit it. See [Editing in the apps](./editing).
