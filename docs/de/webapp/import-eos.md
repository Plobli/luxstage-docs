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
