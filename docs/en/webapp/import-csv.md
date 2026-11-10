# Import CSV

Imports channel data from a CSV file. Suitable for importing from Excel or other tools.

## CSV format

- **Delimiter:** Semicolon (`;`)
- **Encoding:** UTF-8
- **First row:** Header row, skipped during import
- **Column order** (the first six columns are fixed):

| Position | Column |
|----------|--------|
| 1 | Channel |
| 2 | Dimmer address |
| 3 | Fixture |
| 4 | Position |
| 5 | Colour |
| 6 | Notes |

The import also reads **Colour 2**, **Quantity**, **Priority** and **Hint** (`1`/`0`) when they appear in the header row, exactly as the [CSV export](./export-csv) writes them. If they are missing, nothing changes.

Rows without a channel number are skipped.

## Behaviour with existing channels

The import **merges and updates selectively** instead of replacing the entire channel list:

- If a channel with the same number already exists, only the **non-empty** fields from the CSV are applied — empty cells leave existing values unchanged.
- Channels new to the CSV are added.
- After import, the list is sorted numerically by channel number.

::: tip Alternative: scan a channel list
If you don't have a CSV file but do have a photo of a filled-out channel list (printed template or handwritten), it can also be read via AI — see [Scan Channel List](./scan-channel-list).
:::
