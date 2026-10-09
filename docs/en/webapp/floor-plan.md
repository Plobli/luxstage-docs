# Drawing

The **Drawing** tab provides an interactive vector editor for the stage plan. Fixture positions can be drawn in, labelled and exported.

## User interface

### Toolbar

All tools carry a text label next to the icon and are grouped (navigation, draw, lighting, scale, background, export).

| Icon | Tool | Keyboard shortcut |
|------|------|-------------------|
| ▶ Arrow | **Select** | V |
| ✋ Hand | **Pan** | H |
| \ Line | Draw **line** | L |
| □ Rectangle | Draw **rectangle** | R |
| ○ Ellipse | Draw **ellipse/circle** | E |
| T Text | Add **text** | T |
| ⊙ Circle | **Place channel** | C |
| ↑ Upload | **Upload background image** | – |
| ⊠ Remove | **Remove background image** | – |
| ↓ Export | **Export as PNG** | – |

### Bottom tools

| Icon | Function | Keyboard shortcut |
|------|----------|-------------------|
| ↩ | **Undo** | Ctrl+Z |
| ↪ | **Redo** | Ctrl+Y / Ctrl+Shift+Z |
| 🗑 | **Delete selection** | Delete / Backspace |

More keyboard shortcuts for the drawing editor: see [Keyboard Shortcuts](./keyboard-shortcuts).

### Options bar (top left)

| Option | Function | Keyboard shortcut |
|--------|----------|-------------------|
| **Grid** | Show/hide grid | G |
| **Snap** | Enable/disable snap to grid | – |

## Place channels on the drawing

1. Select the **"Place channel" (C)** tool
2. Click on the desired position on the drawing
3. The channel appears as a slim numbered marker. Before clicking, the preview at the cursor already shows the real size

## Rotate elements

Bars, rectangles, ellipses and text can be rotated freely: select the element and drag the yellow handle above it. Alternatively, the buttons in the options bar rotate by 45° or 90° left or right. Channel markers no longer have an orientation.

## Bay frame

Bay frames appear compact with a readable label on an opaque background.

## Scale tool

The scale must be set right after uploading a floor plan. A hint explains the steps and offers **Mark distance** or **Later**. While marking, a line follows the cursor.

1. Select the **Scale** tool
2. Click two points with a known real distance
3. Enter the distance in metres and confirm

Bars and bay frames are then shown at their real size; the placement preview has the same size as the placed element.

## Using a background image

A background image (e.g. a scan of the stage plan) can be added in two ways:

- **Via the template drawing:** Stored in the venue template and automatically inherited by all shows
- **Manually:** Click the **↑ Upload** icon in the toolbar → select an image file

Allowed formats: **PNG, JPG, SVG, WebP**. A PDF stage plan is not supported and must be converted first — an incorrect format shows "Invalid file type. Allowed: PNG, JPG, SVG, WebP".

::: warning Only one background image per template
A new background image replaces the old one immediately, without confirmation. Unlike photos in the Photos tab, the background image is **not compressed or resized** — a large scan stays at full size and is reloaded every time the drawing is opened. For faster loading, it's worth resizing the image yourself beforehand.
:::

To remove: click the **⊠** icon.

## Export as PNG

Click the **↓** icon in the toolbar → the current drawing is downloaded as a PNG file.

::: info Note
For export as PDF (incl. channel list) use **Export → PDF** in the top menu bar.
:::
