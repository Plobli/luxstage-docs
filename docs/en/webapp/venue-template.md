# Venue Template

A venue template contains the fixed channel structure of your stage — fixtures, DMX addresses, positions and note sections. Once created, you can apply it to any new production with a single click.

## Import a venue template from CSV

The fastest method: import an existing channel list as a CSV file.

1. Navigate to **Templates** in the sidebar.
2. Click **"Upload CSV"**.
3. Select your CSV file (semicolon-separated, e.g. from Excel or ETC EOS).
4. Enter a name for the venue template in the **"Name"** field.
5. Click **"Import venue template"**.
6. Close the dialog with **"Close"**.

The venue template is now saved and available for every new show.

## CSV format

The CSV file should contain the following columns:

| Column | Description |
|--------|-------------|
| Channel | Channel number |
| DMX | DMX address |
| Fixture | Fixture type (e.g. "PAR 64", "Profile 1.2 kW") |
| Position | Hanging point or location |
| Gel | Colour filter code (e.g. R02, L201) |
| Note | Free-text note |

::: tip Import EOS export directly
CSV exports from ETC EOS can be imported directly — active channels are recognised automatically.
:::

## Create a venue template manually

Alternatively, you can build a venue template directly in LuxStage:

1. Click **"New venue template"**.
2. Enter name and basic data.
3. Add channels manually or import them later via CSV.

## Rename a venue template

Click the **pencil icon** next to the name to open an input field. Enter the new name, then confirm with **Enter** or by clicking outside. All shows assigned to this venue template will automatically adopt the new name.

## OSC IP address

The detail view of a venue template includes the **OSC IP** field. Enter the IP address of the EOS lighting console for this stage here (e.g. `192.168.1.10`). The field is optional — leaving it empty means no OSC.

The IP address applies to all users and devices working with this venue template. The EOS User ID is set separately per device in the iOS app.

## Templates overview

The overview shows each venue template as its own **card** (not a list/table layout) with:

- **Name** of the venue template
- **Channel count** — number of stored channels
- **OSC IP** — configured IP address (if set)
- **Last modified** — date of the last change

Each card offers the buttons:

- **"Blank form (PDF)"** — downloads a blank, printable channel list for this venue template, e.g. for filling in by hand before a [channel list scan](./scan-channel-list)
- **"Edit"** — opens the venue template's detail view
- **"Delete"** — permanently deletes the venue template after confirmation

## Setup (Lighting Towers & Battens)

The venue template also stores the physical stage structure:

- **Lighting Towers** – slots for fixtures
- **Fly System** – battens, trusses, and point hoists with positionable fixtures

These can be added directly to the template and are then optionally inherited when creating a new show.

## Use a venue template for a new production

When creating a new show, select a venue template. The channel structure and note sections are automatically inherited — you can then customise them individually per show.

## Assign a show to a venue template afterwards

On the show card in the overview, the **pencil icon** opens a dialog for template assignment. The venue template can be changed there — the show's channels remain unchanged; only the metadata (venue name, OSC settings) is updated.

## Apply template changes to existing shows

If a venue template was later extended with sections or lighting towers, these additions can be applied to **all** shows assigned to that template:

1. Click **"Apply to all shows"** (for sections or lighting towers)
2. The dialog names the affected shows before anything happens
3. Confirm — a result reports how many shows were checked and how many elements were added

::: tip Safe operation
Only **missing** elements are added. Sections, battens, or lighting towers a show already has remain unchanged — nothing is overwritten or deleted.
:::

## Circuit groups in the template

The template's **Groups** tab lists all circuit groups (e.g. "Backlight" = 137-148) with their circuits at a glance. Click a group to edit it; **Groups** creates new ones, just like in a show. Groups belong to the template and are matched by **circuit number**.

- New show from the template with channel import: the groups come along.
- Existing shows: **"Apply groups to all shows"** adds groups that are still missing in the show (matched by name). Existing groups stay unchanged. Circuits that do not exist in the show are skipped.

## Compare the channel list with the template

Template changes can be applied to the channel list from within the show:

1. In the show, open the import (dialog **"Choose import source"**) and select **"Compare with template"**. The option only appears if the show is assigned to a venue template.
2. The comparison shows what changes: **Devices changed**, **Addresses changed**, **Quantity changed** and **New channels (only in template)**.
3. The selection starts empty. Tick the changes you want and click **"Apply"**.

Saving works like any other channel list change, and undo still applies. If the channel list already matches the template, the app says so.

::: warning Empty values overwrite
If a value is empty in the template, the show's value is cleared when applied.
:::

## Colour 2 in the template

The template also stores the **2nd gel** (column "2nd gel"). It comes along when you create a show. You decide per show whether to use it.

## Locations in the template

The **Locations** tab of the template stores locations with name, type, place, note and assigned channels. Channels are matched by **channel number**.

- New show from the template with channel import: the locations come along.
- Existing shows: **"Apply locations to all shows"** adds missing locations. Existing ones stay unchanged.

## Save a show's channels as a template

Use **"Save channels as template"** in the show menu. Saved: channel, address, fixture, position, colour, colour 2, note and quantity. Priority and hint stay in the show. Optionally tick **"Save locations too"**.

- **Replace template channels:** all channels in the template are replaced by those of the show.
- **Merge by channel number:** matching numbers are overwritten, new ones added. Other template channels stay.

::: warning Replace deletes
Replacing removes the template's previous channels.
:::
