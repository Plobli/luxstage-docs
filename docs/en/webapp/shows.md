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
3. **Areas** – enable lighting towers and/or battens; with a template selected, also pick its sections individually and optionally import the template's channel list
4. **Lighting towers** (only if a template is selected, the "lighting towers" area is enabled, and the template has any) – pick individual towers from the template
5. **Fly system** (only if a template is selected, the "battens" area is enabled, and the template has any) – pick individual elements from the template

Finally, a **summary** shows all selected values; clicking **"Create Show"** creates the show.

::: tip Note
If a template is selected, the new show optionally inherits the channel structure, selected sections, lighting towers and battens of the chosen venue.
:::

## Open a show

Simply click on the desired show row. The show opens in the **Channels** tab by default, but remembers the last tab you worked in — e.g. if the show was last edited in the Fly System tab, it reopens there next time.

## Edit area settings after creation

The **"Edit"** button next to the show name opens a dialog to:
- Enable/disable areas (lighting towers, battens)
- Select which sections, towers, or battens from the venue template to include

## Change show metadata afterwards

In the opened show, the **show name** can be clicked and edited directly. Clicking the **date** (or "Info", if no date is set yet) next to the name opens a dialog to edit date and season.

## Archive a show

Hovering over a show row reveals an **archive icon** on the right. After confirming, the show disappears from the home page and appears in the **Archive**.

::: warning Note
Archiving can be undone in the archive. Permanent deletion is possible via the archive section.
:::

## Demo show

Every new team gets a **demo show** to try things out. It appears in the show list with a **"Demo"** badge and contains sample data for the channel list, towers, battens, locations and floor plan.

- **Editing is allowed** – try anything in the demo show.
- **Reset** – the **"Reset"** button in the banner at the top of the show restores the original state for everyone in the team.
- **Hide** – hovering over the row shows an eye icon that hides the demo show **for you only**. Bring it back via **Help → "Show demo show"**.
- **Cannot be deleted** – the demo show can be neither archived nor deleted, not even by an administrator.

::: tip Teams without a demo show
Teams created before the demo show was introduced get it via **Help → "Show demo show"**.
:::

## Tour of the demo show

On first start, LuxStage offers you the demo show with a short **tour**. You can take it or skip it with **"Look around myself"**. The tour never starts on its own.

A small window appears right at the relevant spot and shows the way to your own show in six stations:

1. **Create a show** – this is where you start your own show later.
2. **Bring in channels** – in the demo the channels are already there. In your own show they come from the console or from a file.
3. **Edit channels** – the tour goes through the columns one by one: **channel number and address**, **color**, **quantity and device**, **notes**, **prio** and **position**. The column in question is in the light.
4. **Areas of the show** – here you switch between setup notes, towers, fly system, photos, drawing and the other areas.
5. **Focus with your phone** – you connect your phone with a code. In the demo this is only a preview.
6. **Print the list** – the channel list as a PDF.

The place of the current station sits in a soft spotlight, the rest of the interface is dimmed. You can click yourself at any time. **"Next"** and **"Back"** change the station, **"Close"** ends the tour.

- **After an interruption** the tour continues where you stopped. The progress belongs to your user account.
- **Watch it again** – via **Help → "Watch the tour again"**. If the demo show is hidden, this entry shows it again.
- **At the end** LuxStage asks whether you want to create your own show or look around a bit more. Without an account, **"Create my own show"** leads to registration.
- The tour is available in the web app and the desktop app from a window width of 768 pixels, not in the smartphone apps.

## Demo without an account

You can try the web app at **demo.luxstage.app** without an account, also in the desktop app via **"View demo"**. Everyone gets their own copy of the demo show. The demo needs an internet connection.

- The copy is deleted after **20 minutes of inactivity**. The demo then offers a restart.
- **Reset** restores the original state at any time.
- The lighting plan can be viewed as a **PDF preview** but not downloaded. CSV export is not available either.
- Also not available: uploading photos, import, settings, team, users and billing.
