# CSV exportieren

Exportiert die Kreisdaten als **CSV-Datei** – kompatibel mit Microsoft Excel, Google Sheets und anderen Tabellenkalkulationen.

- **Trennzeichen:** Semikolon (`;`)
- **Encoding:** UTF-8
- **Dateiname:** `<Show-ID>-kanäle.csv`
- **Spalten** (in dieser Reihenfolge): Kreis, Dimmer-Adresse, Gerät, Bühnenposition, Gel, Notizen, danach **Farbe 2** (nur wenn die Show die 2. Folie nutzt), **Anzahl**, **Prio** und **Hinweis** (`1` = Kreis ist ein Hinweis, sonst `0`)

Das Format entspricht exakt dem des [CSV-Imports](./import-csv) — eine exportierte Datei lässt sich unverändert wieder importieren.

**Hinweis:** Der Export enthält **immer alle Kreise** der Show, unabhängig von aktiven Suchfiltern oder Health-Status-Filtern in der aktuelle Ansicht.

::: tip Tipp
CSV-Export eignet sich gut für den Datenaustausch mit dem Lichtpult oder für eigene Auswertungen.
:::
