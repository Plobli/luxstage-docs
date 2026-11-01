# Scan Channel List

In addition to the [EOS import](./import-eos) and [CSV import](./import-csv), there's a third way to fill in a channel list: upload a photo of a filled-out channel list and have it read automatically by AI.

::: tip Download the template first
The channel list template works best for scanning. Download and print it under **Templates**, fill it in (e.g. by hand on setup day), and then photograph it. A fully handwritten list without a template also works.
:::

## Upload a photo

1. In LuxStage, click **"Import"** → select **"Scan channel list"**
2. Choose the photo of the filled-out channel list from your file system
3. The AI reads the image — a "Reading channel list …" notice appears while processing

## What gets read?

The AI recognizes as many of the following fields per row as are legible in the photo:

- **Channel number** (required — a row can't be applied without it)
- **Address** (DMX address)
- **Fixture**
- **Position** — even if it only appears once as a group heading spanning multiple rows, instead of per row
- **Filter/color**
- **Notes**

Channels already present in the show act as a reading aid for the AI (e.g. to resolve unclear handwriting more plausibly) — they are not automatically changed by this; that only happens via the preview.

::: warning Photo quality
Handwriting may not always be read cleanly. Where unclear, the AI picks the most plausible reading. Check the results in the preview before applying them.
:::

## Preview and selection

After processing, a **"Scan Channel List — Preview"** dialog opens with up to two groups:

- **Updated channels** — existing channels where the scan detected a change
- **New channels** — channels recognized in the scan that don't yet exist in the show

Each detected change can be **deselected individually** before it is applied. The **"Toggle all"** button flips the selection of all rows at once.

If no filled-out rows were recognized in the photo, the notice "No filled-out rows detected." appears.

## Apply

Clicking **"Apply"** applies only the selected changes. A confirmation shows how many channels were updated and how many were newly created.

::: warning Photo is sent to the Anthropic API
The scan uses an AI model from Anthropic (Claude Vision). The uploaded photo is sent to the Anthropic API for this purpose — unlike the rest of the web app's features, which communicate exclusively with your own LuxStage server. See the [Privacy Policy](../privacy#scan-channel-list-ai-photo-scan) for details.
:::
