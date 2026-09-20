# Aufbaunotizen, Raum & Hinweise

Anders als der Name vermuten lässt, gibt es in der App **keinen einzelnen „Info"-Tab**. Jede Sektion der Spielort-Vorlage erscheint stattdessen als **eigener Eintrag in der Sidebar** der Show — z. B. „Aufbaunotizen", „Raum" oder „Hinweise". Über **„+ Bereich"** lassen sich weitere Sektionen hinzufügen.

## Sektionstypen

Jede Sektion hat einen von zwei Typen:

### Text

Freitext-Bereich mit Formatierung — für Beschreibungen, Besonderheiten oder offene Punkte. Die Standard-Sektion **„Aufbaunotizen"** ist von diesem Typ.

### Felder

Tabelle mit strukturierten Schlüssel-Wert-Paaren für technische Daten, z. B. Raummaße oder Hängehöhen.

## Textbereiche bearbeiten

Die Werkzeugleiste über jedem Textbereich bietet folgende Formatierungen:

| Button | Funktion |
|--------|----------|
| **B** | Fett |
| *I* | Kursiv |
| **H** | Überschrift |
| ≡ | Aufzählungsliste |
| 1. | Nummerierte Liste |
| ⊞ | Tabelle einfügen (mit Buttons zum Hinzufügen/Löschen von Zeilen und Spalten) |

Einfach in den Textbereich klicken und tippen. Änderungen werden automatisch gespeichert.

## Felder-Bereiche

Abschnitte vom Typ **„Felder"** zeigen eine Tabelle mit strukturierten Zeilen (Label/Wert).

- **+ Feld** – Neue Zeile hinzufügen
- **+ Textfeld** – Einen neuen Bereich vom Typ Textfeld/Markdown anlegen (kein Textblock innerhalb des aktuellen Abschnitts)

::: tip Nur ein Felder-Bereich pro Show
Pro Show ist nur **ein** Bereich vom Typ „Felder" möglich — ist er bereits angelegt, verschwindet der entsprechende Button im Anlege-Dialog.
:::

## Eigenen Bereich anlegen

1. Klick auf **„+ Bereich"** in der Sidebar
2. Typ wählen: **Text** oder **Felder**
3. Namen vergeben (z. B. „Rigging") und bestätigen

## Bereiche schließen

Jeder Bereich hat ein **×**-Symbol oben rechts zum Löschen der Sektion. **Warnung:** Das Löschen ist unwiderruflich und kann nicht rückgängig gemacht werden — bitte mit Bedacht verwenden.

## Automatisch generierter Text bei Aufbaunotizen

Im Bereich **„Aufbaunotizen"** erscheint unterhalb der eigenen Notizen ein schreibgeschützter Bereich mit automatisch generiertem Text — separat für **Beleuchtungsgestelle** und **Obermaschinerie** (Zugstangen), sofern im Setup ([Beleuchtungsgestelle](./setup-gestelle) bzw. [Zugstangen](./setup-zugstangen)) Daten hinterlegt sind. Der Text fasst die belegten Bühnenpositionen, Kreise, Geräte und Farben zusammen und lässt sich markieren und kopieren (z. B. für Cue-Sheets oder E-Mails an die Regie) — es gibt keinen eigenen Kopieren-Button, nur die browserübliche Textmarkierung. Er wird nicht manuell bearbeitet, sondern aktualisiert sich automatisch mit den Setup-Daten.
