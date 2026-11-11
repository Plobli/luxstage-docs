# Export CSV

Exports the channel data as a **CSV file** – compatible with Microsoft Excel, Google Sheets and other spreadsheet applications.

- **Delimiter:** Semicolon (`;`)
- **Encoding:** UTF-8
- **Filename:** `<show-id>-kanäle.csv`
- **Columns** (in this order): Channel, Dimmer address, Fixture, Position, Gel, Notes, then **Colour 2** (only if the show uses the 2nd gel), **Quantity**, **Priority** and **Hint** (`1` = channel is a hint, otherwise `0`)

The format exactly matches [CSV import](./import-csv) — an exported file can be re-imported unchanged.

::: tip Tip
CSV export is well suited for exchanging data with the lighting console or for custom analysis.
:::
