# Aus Eos importieren

Importiert Kreisdaten direkt von einem **ETC EOS**-Lichtpult. Dabei werden alle Kreise, welche im Pult in Stimmungen gespeichert sind, in der Kreistabelle gelb markiert. Zusätzlich übernimmt der Import — sofern in der Exportdatei vorhanden — DMX-Adresse und Gerätebezeichnung, und erkennt automatisch Moving Lights.

Der EOS-Export muss wie folgt konfiguriert werden:

- Setup → Exportieren → CSV → Speicherort wählen
- Im Export-Dialog: „Stimmungen", „Werte" und „Patch" aktivieren

![EOS Export-Dialog](/img/webapp/import-eos/eos-export-dialog.png)

- In LuxStage auf **„Importieren"** klicken — ein Auswahldialog erklärt den Unterschied zwischen „Aus Eos importieren" und „CSV importieren" und öffnet nach Auswahl den Datei-Dialog
- Exportierte CSV-Datei auswählen
- Import im Merge-Dialog überprüfen

![Merge-Vorschau](/img/webapp/import-eos/merge-vorschau.png)

## Merge-Dialog

Der Merge-Dialog zeigt bis zu fünf Gruppen:

- **Neu aktiv** — Kreise, die im Pult neu bespielt werden. Jede Kreisnummer ist anklickbar: ein Klick schließt den Kreis vom Import aus (er wird rot und durchgestrichen dargestellt). Ausgeschlossene Kreise bleiben **dauerhaft** ausgeschlossen — auch bei künftigen Importen —, bis sie wieder angeklickt werden. „Alle übernehmen" / „Keine übernehmen" wählen alle Kreise auf einmal.
- **Nicht aktiv in der importierten Show** — vormals aktive Kreise, die im aktuellen Export fehlen
- **Unverändert** — bereits beschriftete Kreise, die der Import **nicht** überschreibt
- **Adresse weicht ab** — nur sichtbar, wenn ein Kreis bereits eine DMX-Adresse hat, die vom Export abweicht. Ein Pfeil-Symbol pro Kreis legt fest, ob die alte oder die neue Adresse übernommen wird; „Alle übernehmen" / „Keine übernehmen" gelten für alle abweichenden Adressen auf einmal.
- **Gerät weicht ab** — funktioniert wie „Adresse weicht ab", nur für die Gerätebezeichnung

::: tip Bestehende Notizen bleiben erhalten
Der Import löscht nichts: Geräte, Farben und Notizen bleiben in allen Kreisen erhalten. Fehlende Kreise werden neu angelegt, nicht mehr aktive nur als inaktiv markiert. Das gilt auch beim wiederholten Import (Re-Import) derselben Show.
:::

::: tip Leere Felder werden automatisch übernommen
Hat ein Kreis noch keine DMX-Adresse oder kein Gerät eingetragen, übernimmt der Import den Wert aus dem Export automatisch — ganz ohne Rückfrage. Nur bei bereits **vorhandenen, abweichenden** Werten entscheidet die/der Nutzer:in im Merge-Dialog.
:::

Gibt es keine Änderungen gegenüber dem aktuellen Stand, erscheint „Keine Änderungen." — der Import lässt sich trotzdem bestätigen.

- Import mit Klick auf „Importieren" starten

## Moving Lights

Fixtures mit Pan/Tilt-Funktion (laut Export) gelten als Moving Light. Neu angelegte oder neu aktive Kreise ohne Notiz erhalten automatisch die Notiz „Moving Light" und erscheinen damit grün statt gelb — Moving Lights leuchten pro Show meist viele unterschiedliche Bühnenpositionen aus, eine feste Positions-Notiz ist für sie nicht sinnvoll.

Alle übrigen gelb markierten Kreise können nun in der Kreistabelle mit Notizen, Farbcode etc. beschriftet werden.

## Direkt vom Pult holen

Nur in der [Desktop-App](/de/webapp/desktop-app): Statt einer CSV-Datei holst du den Patch direkt aus dem Pult.

1. In Eos: Setup › System › Show Control › OSC, „OSC TCP“ aktivieren (Port 3037). Rechner und Pult müssen im selben Netz sein.
2. In LuxStage auf **„Importieren"** klicken und **„Vom Pult holen"** wählen.
3. Adresse des Pults eingeben (z. B. `192.168.1.20`) und **„Abrufen"** klicken.
4. Modus wählen. Die Vorschau zeigt, was sich ändert.
5. Mit **„Übernehmen"** bestätigen.

| Modus | Wirkung |
|-------|---------|
| **Nur Neues** | Legt nur Kreise an, die in der Liste noch fehlen. |
| **Zusammenführen** | Legt neue Kreise an, aktualisiert Adresse und Gerät. Farbe, Position, Notizen und Fotos bleiben. |
| **Pult spiegeln** | Wie Zusammenführen, entfernt aber Kreise, die im Pult nicht gepatcht sind. Dafür musst du die Anzahl der zu entfernenden Kreise ausdrücklich bestätigen. |

::: tip Rückgängig möglich
Der Abgleich läuft wie jede andere Änderung. Du findest ihn im Verlauf und kannst ihn mit Widerrufen zurücknehmen.
:::

::: info Nur der Patch
Vom Pult kommen Kreise, Adressen und Geräte. Die Werte der Stimmungen liefert das Pult nicht. Dafür bleibt der CSV-Import (oben).
:::

Meldet LuxStage, das Pult habe nicht alle Kreise geliefert, ruf erneut ab.
