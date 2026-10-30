# Desktop-App

Die Desktop-App für Mac und Windows zeigt dein Team in einem eigenen Fenster. Sie verhält sich wie ein normales Programm: eigene Menüleiste, Tastenkürzel, Fensterposition wird gemerkt. Zusätzlich holt sie den Patch direkt aus dem Eos-Pult.

## Installation

- **Windows:** [Microsoft Store](https://apps.microsoft.com/detail/9n4d59hvlwn0?hl=de-DE). Updates kommen automatisch.
- **Mac:** [Download der aktuellen Version](https://github.com/Plobli/luxstage-desktop/releases/latest) (Datei `…-arm64.dmg`, für Macs mit Apple-Chip). Die App ist signiert und von Apple geprüft und aktualisiert sich selbst.

Beim ersten Start gibst du den Namen deines Teams ein, zum Beispiel `mein-theater` für `mein-theater.luxstage.app`. Über **Team wechseln …** im Menü wechselst du später das Team. Ein neues Team legst du direkt auf der Startseite an.

## Menüleiste

Importieren, Exportieren, Verlauf, Suchen sowie Rückgängig und Wiederholen findest du in der Menüleiste. In der Kopfzeile der Show erscheinen diese Knöpfe deshalb nicht noch einmal.

| Menü | Befehl | Mac | Windows |
|------|--------|-----|---------|
| Ablage (Windows: Show) | Importieren … | ⌘I | Ctrl+I |
| | Als PDF exportieren … | ⇧⌘E | Ctrl+Shift+E |
| | Als CSV exportieren | | |
| | Verlauf anzeigen | ⌘Y | Ctrl+H |
| Bearbeiten | Widerrufen | ⌘Z | Ctrl+Z |
| | Wiederholen | ⇧⌘Z | Ctrl+Y |
| | Suchen … | ⌘F | Ctrl+F |
| Navigation | Zurück / Vor | ⌘[ / ⌘] | Ctrl+[ / Ctrl+] |

In Textfeldern gelten Widerrufen und Wiederholen für den eingegebenen Text, sonst für die Show. Einstellungen öffnest du mit ⌘, (Mac) beziehungsweise Ctrl+, (Windows).

## Werkzeugleiste

Undo/Redo, Filter und Suche sitzen oben in der Kopfzeile neben dem Show-Namen. Auf dem Mac ist die Kopfzeile zugleich die Titelleiste, du kannst das Fenster dort ziehen. Die Suche findest du in der Kreisliste, bei Gassentürmen, Obermaschinerie, Standorten und Fotos. In den übrigen Ansichten ist sie ausgegraut.

## Pult-Sync mit Eos

Mit der Desktop-App holst du den Patch direkt aus dem Pult. Neue Kreise, Adressen und Geräte landen ohne Export-Datei in der Kreisliste. Du wählst, ob nur Neues ergänzt, zusammengeführt oder das Pult gespiegelt wird. Details: [Aus EOS importieren](/de/webapp/import-eos).
