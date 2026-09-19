# Shows

## Shows overview

The home page shows all existing shows as a sortable list. Each row contains:

- **Name** – Show name, e.g. "Hamlet"
- **Date** – Performance date, e.g. "04/30/2026"
- **Season** – e.g. "25/26" (visible from the lg breakpoint)
- **Last edited by** – Email address of the last person to edit the show
- **Archive button** – appears on the right when hovering over the row

The list can be sorted by clicking the column headers (Name, Date, Season, Last edited by). By default, the list is sorted by **"Date" descending** (newest first), not alphabetically. An arrow (↑/↓) on the column header shows the active sort direction; clicking again reverses it. "Name" defaults to ascending, all other columns default to descending.

Shows are grouped by venue, with the venue name as a heading. Shows without an assigned venue appear under "—". Sorting applies **within** each venue group — the groups themselves are always alphabetical, regardless of the chosen sort order.

::: tip Columns depend on window width
"Season" only appears from medium screen width, "Date" and "Last edited by" only from small screen width. On narrow screens (e.g. a tablet in portrait mode), fewer columns are visible accordingly.
:::

## Create a new show

Clicking **"New Show"** (button in the bottom right) starts a multi-step wizard. Depending on your choices, it runs through up to five steps:

1. **Template** – select an existing venue template, or "No template"
2. **Name & date** – name, date, optional season (e.g. "25/26")
3. **Areas** – enable lighting towers and/or bars; with a template selected, also pick its sections individually and optionally import the template's channel list
4. **Lighting towers** (only if a template is selected, the "lighting towers" area is enabled, and the template has any) – pick individual towers from the template
5. **Fly system** (only if a template is selected, the "bars" area is enabled, and the template has any) – pick individual elements from the template

Finally, a **summary** shows all selected values; clicking **"Create Show"** creates the show.

::: tip Note
If a template is selected, the new show optionally inherits the channel structure, selected sections, lighting towers and bars of the chosen venue.
:::

## Open a show

Simply click on the desired show row. The show opens in the **Channels** tab by default, but remembers the last tab you worked in — e.g. if the show was last edited in the Fly System tab, it reopens there next time.

## Change show metadata afterwards

In the opened show, the **show name** can be clicked and edited directly. Clicking the **date** (or "Info", if no date is set yet) next to the name opens a dialog to edit date and season.

## Archive a show

Hovering over a show row reveals an **archive icon** on the right. After confirming, the show disappears from the home page and appears in the **Archive**.

::: warning Note
Archiving can be undone in the archive. Permanent deletion is possible via the archive section.
:::
