# CSV importieren

Importiert Kreisdaten aus einer CSV-Datei. Geeignet für den Import aus Excel oder anderen Tools.

## CSV-Format

- **Trennzeichen:** Semikolon (`;`)
- **Encoding:** UTF-8
- **Erste Zeile:** Kopfzeile, wird beim Import übersprungen
- **Spaltenreihenfolge** (feststehend, keine Namens-Erkennung):

| Position | Spalte |
|----------|--------|
| 1 | Kreis |
| 2 | Dimmer-Adresse |
| 3 | Gerät |
| 4 | Bühnenposition |
| 5 | Farbe |
| 6 | Notizen |

Zeilen ohne Kreisnummer werden übersprungen.

## Verhalten bei bestehenden Kreisen

Der Import **ergänzt und überschreibt gezielt**, statt die komplette Kreisliste zu ersetzen:

- Gibt es bereits einen Kreis mit derselben Kreisnummer, werden nur die **nicht-leeren** Felder aus der CSV übernommen — leere Zellen lassen bestehende Werte unverändert.
- Kreise, die in der CSV neu sind, werden zusätzlich angelegt.
- Nach dem Import wird die Liste numerisch nach Kreisnummer sortiert.

::: tip Alternative: Kreisliste scannen
Liegt keine CSV-Datei vor, aber ein Foto einer ausgefüllten Kreisliste (Vordruck oder handschriftlich), lässt sich diese auch per KI auslesen — siehe [Kreisliste scannen](./scan-kreisliste).
:::
