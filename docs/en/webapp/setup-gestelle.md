# Setup — Lighting Towers

The **Setup** area manages the physical structure of the stage. This page covers **lighting towers** (towers with numbered slots) — for battens, see [Setup — Battens](./setup-zugstangen).

::: tip Not to be confused
This area is not the same as the "Aufbau" tab in the iOS app – that one shows checklists and free-text notes from the [Setup Notes](./info) section.
:::

::: tip The term "Truss"
The in-app help text for lighting towers also gives "towers or trusses beside the stage" as an example — this refers to side towers with slots as described here. The standalone **"Truss"** element type under [Setup — Battens](./setup-zugstangen) is different: a freely positionable batten in the fly system.
:::

Depending on the show's settings (see [Shows](./shows)), one, the other, or both areas appear as their own sub-tab within Setup: lighting towers as "Lighting Towers", battens as **"Fly System"**.

## Create a tower

1. Click **"New Lighting Tower"** (bottom right)
2. Fill in the fields:

| Field | Description |
|-------|-------------|
| **Name** | Name of the tower, e.g. "Lighting Tower 1" |
| **Number of slots** | How many tower positions the tower has (1–20) |

3. Click **"Create"**

## Channel list rail

Next to towers and overhead rigging, the **channel list rail** sits on the right, showing fixture, colour and note of each channel. It offers:

- **Search** by channel number or fixture
- **All / Unplaced** filter
- **Eye button** "Only channels with note"
- **Stage position filter** with counter
- **Placement pill** per channel, e.g. "Tower 1 · S1, S3"

The list stays stable; a channel can be placed several times. The rail can be dragged wider.

## Assign a channel to a slot

**With the rail:**

1. Click a slot or a channel, then its counterpart. Alternatively drag a channel from the rail onto the slot.
2. After a slot, the target jumps to the next free slot. A selected channel stays selected until you press **Esc** or click outside tower and rail.
3. If a channel is missing, **Enter** in the search creates an unknown number in the channel list.

The rail does not ask before overwriting an occupied slot; **Undo** still applies.

**Without the rail** (template editor, narrow screens, collapsed rail):

1. Click the **⌄⌄** (select) icon on the right of a slot
2. Search by channel number or fixture in the search field
3. Click a channel → it is assigned to the slot

If the next slot is still empty, its selection dialog opens automatically. If a slot is already occupied, a confirmation appears before overwriting.

## Clear a slot

Click the **×** icon next to an occupied slot.

## Swap slots via drag & drop

Using the grip icon (⠿) to the left of the slot number, the channel assignment of two slots can be swapped via drag & drop.

## Add a slot

Click **"Add slot"** below the rig's slot list.

## Edit / delete a tower

Using the icons in the top right of each tower card:

- **Pencil** – change name, side, or number of slots. Reducing the slot count shows a warning listing the affected (possibly occupied) slots.
- **Trash** – delete the tower after confirmation

## Note per slot

Each slot has its own **Setup note** field (separate from the channel list note used for focusing). Enter text; it is saved when you leave the field.

## Add a note

At the bottom of each tower card, click **"+ Note"** to add a free-text comment.

## Save as template

The bookmark icon lets you save a tower into the venue template. You can choose to include the base structure (always included), plus channel number, fixture, and colour per slot.

::: tip Note
Lighting towers from the template are not inherited automatically when quickly creating a show — only the creation wizard lets you select them individually, or you can add them later via "Insert" in the edit dialog.
:::
