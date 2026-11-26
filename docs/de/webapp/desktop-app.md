# Desktop-App

Die Desktop-App für Windows zeigt dein Team in einem eigenen Fenster. Sie verhält sich wie ein normales Programm: eigene Menüleiste, Tastenkürzel, Fensterposition wird gemerkt. Zusätzlich holt sie den Patch direkt aus dem Eos-Pult.

## Installation

- **Windows:** [Microsoft Store](https://apps.microsoft.com/detail/9n4d59hvlwn0?hl=de-DE). Updates kommen automatisch.

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
| Ansicht | Neu laden | ⌘R | Ctrl+R |
| | Vollbild, Zoom | | |
| Hilfe | Tour noch einmal ansehen | | |
| | Dokumentation | | |
| | Fehlerberichte senden | | |
| | Offline-Speicher leeren | | |

In Textfeldern gelten Widerrufen und Wiederholen für den eingegebenen Text, sonst für die Show. Einstellungen öffnest du mit ⌘, (Mac) beziehungsweise Ctrl+, (Windows).

## Werkzeugleiste

Undo/Redo, Filter und Suche sitzen oben in der Kopfzeile neben dem Show-Namen. Auf dem Mac ist die Kopfzeile zugleich die Titelleiste, du kannst das Fenster dort ziehen. Die Suche findest du im Einleuchtplan, bei Gassentürmen, Obermaschinerie, Standorten und Fotos. In den übrigen Ansichten ist sie ausgegraut.

## Pult-Sync mit Eos

Mit der Desktop-App holst du den Patch direkt aus dem Pult. Neue Kreise, Adressen und Geräte landen ohne Export-Datei in der Kreisliste. Du wählst, ob nur Neues ergänzt, zusammengeführt oder das Pult gespiegelt wird. Details: [Aus EOS importieren](/de/webapp/import-eos). Auch die Kreisgruppen lassen sich aus dem Pult holen (Kreisliste → Gruppen → „Aus Pult importieren“).

## Ohne Netz

Die Desktop-App merkt sich die Web-App und die Daten deiner Shows auf dem Rechner. Fällt das Netz aus, kannst du Shows weiter lesen. Änderungen brauchen Verbindung zum Server. Der Speicher ist auf 500 MB begrenzt. Mit **Hilfe → Offline-Speicher leeren** löschst du ihn, zum Beispiel auf einem fremden Rechner.

## Fehlerberichte

Auf Wunsch sendet die App bei Abstürzen und Fehlern technische Informationen an den Fehlerdienst Sentry in der EU, ohne Namen, Konten, Shows oder Fotos. Das ist standardmäßig aus. Du schaltest es unter **Hilfe → Fehlerberichte senden** ein, nach einer Rückfrage. Die Änderung gilt ab dem nächsten Start.
