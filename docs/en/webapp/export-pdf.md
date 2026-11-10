# Export PDF

Click the **"Export"** button in the top menu bar of a show → select **"PDF"**. The download starts directly, with no preview dialog.

Exports the complete channel plan as a print-ready **PDF document**. The export contains:

- Show name, date and show time
- Show notes
- **Fly system:** a ruler with the fixtures and a table (number, device, address, position, color, note) for each batten
- **Lighting towers:** a card per tower with fill level and slots
- **Locations:** a setup list of its channels for each location
- Complete channel table with all positions
- Drawing (if present), optionally limited to your own [print area](./floor-plan#set-the-print-area)
- Photos (if present, quantity according to the "Photos per print page" setting)

::: tip How to read the sections
- Multiple fixtures appear as "3x PAR64" at the fixture name. Quantity 1 shows no prefix.
- The **2nd gel** appears as its own colour pill next to the first.
- Battens carry their number ("Zug 7").
- Below each photo you see the channels it belongs to ("Channels: 12, 14, 21").
- A thick line separates **Fly system**, **Lighting towers** and **Locations**.
- Device types keep the same color in every section. The type list at the top of a section shows name and count.
- Filter colors appear as in the web app: a colored pill with its code, frost filters hatched.
- Long device names wrap: two lines in tables, three lines in tower cards.
- The **Note** column only appears when at least one device has a note. Otherwise the table uses the full width.
- A batten or location is only split across pages if it is taller than one page.
:::

::: info Personal notes
Your [personal notes](./channels) are never in the PDF. Only the shared channel notes appear.
:::

::: tip Notes on photos in the PDF
Photos whose file is no longer readable are silently skipped. Long photo captions are truncated to a single line (with "…").
:::

::: info Drawing state in the PDF
The drawing is automatically saved as a snapshot when opened or edited in the Drawing tab. This snapshot is what ends up in the PDF — not necessarily the very latest state, if changes were made to the drawing itself since the last time it was opened.
:::
