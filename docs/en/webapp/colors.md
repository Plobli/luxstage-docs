# Managing Colors

The **Colors** template holds every color filter in your house: the bundled Lee and Rosco filters plus your own colors, for example a frost filter from your stock. Colors apply to all stages, all shows and all PDFs.

## Open it

Under **Templates**, the **Colors** entry sits below the venue templates. Click it to open the list.

## Browse the list

- **Search:** type a code, code 2 or name.
- **Type:** color, frost, diffusion or neutral density.
- **Standard / Custom:** show only bundled or only self-made colors.

Each row shows the code (for standard colors the Lee number followed by the Rosco number), the name, the type and how many channels use the color.

## Edit a color

Click a row to open the dialog. You can change everything: code, code 2, name, type, display color and note. This includes standard colors. Changes apply to every channel list immediately.

If you change a code, all channels using the color follow automatically.

## Add a custom color

1. Click **"New color"**.
2. Enter a code, for example `HF-1`. It must not look like a Lee or Rosco number (no `L201`, `R44` or `201`).
3. Enter a name and choose the type.
4. Pick the display color and save.

Custom colors appear at the top of the color picker in every channel list.

## Frost and diffusion

Frost and diffusion have no real color. LuxStage shows them **hatched** with diagonal lines, in the channel list and in the PDF. The denser the lines, the stronger the diffusion. In the dialog you choose **Light**, **Medium** or **Strong**. The base color underneath is white but can be slightly tinted.

## Reset and delete

- **Reset to standard** restores a changed standard color. The button only appears when the color differs from the standard.
- **Delete** removes a color after a warning. Channels that use it keep their code and all other details. Only the display color is missing.
- **Restore standard colors** re-creates deleted standard colors and adds new filters from the bundled list. Existing and changed colors stay untouched.

## In the apps

The iOS and Android apps load the color list from the server. Offline they use the last loaded state.
