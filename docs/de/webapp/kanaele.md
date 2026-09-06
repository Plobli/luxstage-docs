# Kreise

Der **Kreise**-Tab ist die Hauptansicht einer Show und zeigt den vollständigen Kreisplan.

::: tip Inline-Hilfe in der App
Neben den Spaltenüberschriften der Kreistabelle und im Setup-Bereich zeigen kleine Hilfe-Icons Kurzerklärungen zu den jeweiligen Feldern direkt in der App.
:::

## Live-Zusammenarbeit (Presence)

Arbeiten mehrere Personen gleichzeitig an einer Show, erscheinen oben in der Show-Leiste kleine, farbige Avatare (Initiale) für jede angemeldete Person:

- **Grüner Ring/Punkt** – die Person bearbeitet die Show gerade aktiv
- **📱-Badge** – die Person ist über die iOS-App verbunden
- Tooltip beim Überfahren zeigt Name und verbundene Geräte (iOS und/oder Web)

Die Avatare erscheinen erst ab zwei gleichzeitig verbundenen Personen; bei mehr als vier wird die Zahl der weiteren als „+N" zusammengefasst. Änderungen anderer Nutzer erscheinen in Echtzeit, ohne Neuladen der Seite.

## Aufbau des Kreisplans

Die Tabelle hat fünf Spalten:

| Spalte | Bedeutung |
|--------|-----------|
| **KREIS** | Kreisname im Pult (links) / Dimmer-Adresse (rechts nach dem „/"), z. B. „1/001" |
| **FARBE** | Farbfilter (Gel-Code), z. B. „L201/R371" oder „RGB", „variable" |
| **ANZ.** | Anzahl identischer Geräte an dieser Bühnenposition |
| **GERÄT** | Leuchtenbezeichnung, z. B. „ETC Source Four 26°" |
| **NOTIZEN** | Freitext-Notiz, z. B. „Key light stage left, narrow spot" |

Die Kreise sind nach **Bühnenpositionen** gruppiert (z. B. „FOH BAR LEFT", „OVERHEAD BAR 1", „SIDE BOOM SL"). Die Anzahl der Kreise je Bühnenposition wird als Zahl rechts neben dem Namen der Bühnenposition angezeigt.

## Kreis auswählen und bearbeiten

1. Auf eine Zeile klicken – ein **Drag-Handle** (⠿) erscheint links, ein **×**-Button rechts
2. Felder direkt bearbeiten:

| Feld | Aktion |
|------|--------|
| **Kreiszahl links** | Klicken → Nummer eingeben|
| **Dimmer-Adresse rechts** | Klicken → Adresse eingeben |
| **Farbe** | Klicken → Dropdown mit verfügbaren Gel-Codes erscheint (z. B. „L201 / R371 Full C.T. Blue"). Zusätzlich wählbar: **„No Color"** (kein Farbfilter) oder **Freitext** für eigene Angaben (z. B. „R02" oder „warm weiß") |
| **Gerät** | Klicken → Gerätebezeichnung eingeben |
| **Notizen** | Klicken → Freitext eingeben |

::: tip DMX-Adresse wird automatisch normalisiert
Beim Verlassen des Adressfelds wird die Eingabe automatisch ins Format „Universum/Adresse" gebracht, z. B. wird aus „129" automatisch „1/129" und aus „1/1" wird „1/001". Reine Zahlen über 512 werden dabei als durchlaufende Adresse über mehrere Universen interpretiert (z. B. „515" → „2/003").
:::

## Kreis-Status umschalten

Die **Kreisnummer** erscheint in drei Farben:

- **Weiß** – ohne Notiz und ohne Einbauort
- **Grün** – Notiz vorhanden oder einem Einbauort (Beleuchtungsgestell-Slot bzw. Zugstange) zugewiesen
- **Gelb** – in der Show aktiv (z. B. nach EOS-Import), aber weder Notiz noch Einbauort vorhanden

Dieselbe Legende steht auch als Inline-Hilfe (Hilfe-Icon) neben der Kreistabelle in der App.

## Kreis hinzufügen

Unterhalb jeder Bühnenposition befindet sich der Button **„+ Kreis hinzufügen"**. Ein Klick fügt einen neuen leeren Kreis zur jeweiligen Bühnenposition hinzu.

## Kreis löschen oder leeren

Den Kreis anklicken (aktivieren), dann auf das **×**-Symbol rechts in der Zeile klicken. Ein Dialog bietet zwei Optionen:

- **Kreis leeren** – entfernt nur Notiz und Farbe, die Zeile bleibt bestehen
- **Zeile löschen** – entfernt den Kreis vollständig

## Kreis einem Einbauort zuweisen

Bei Hover über eine Kreiszeile erscheint rechts (vor dem Löschen-Button) der Button **„Zuweisen"** mit drei Optionen:

- **Im Grundriss platzieren** – öffnet den [Grundriss](./grundriss) und platziert den Kreis dort
- **Beleuchtungsgestell-Slot zuweisen** – öffnet [Setup — Beleuchtungsgestelle](./setup-gestelle) zur Zuweisung an ein Gestell
- **Zugstange zuweisen** – öffnet [Setup — Zugstangen](./setup-zugstangen) zur Platzierung auf einer Zugstange

Ist der Kreis bereits einem Gestell-Slot oder einer Zugstange zugewiesen, wird der Einbauort zusätzlich als kleines Badge unterhalb der Notiz angezeigt.

::: tip Warnung bei Duplikaten
Vergibst du eine DMX-Adresse oder Kreisnummer doppelt, warnt die Tabelle mit „Doppelte DMX-Adresse!" bzw. „Doppelte Kreisnummer!".
:::

## Reihenfolge ändern (Drag & Drop)

Per **Drag & Drop** am ⠿-Handle links können Kreise innerhalb einer Bühnenposition neu angeordnet werden.

## Bühnenposition umbenennen

Beim Hovern über eine Bühnenpositions-Überschrift erscheint der Button **„Bühnenposition umbenennen"** – klicken und neuen Namen eingeben.

## Suche

Im Suchfeld oben rechts (**„Suchen …"**) können Kreise, Geräte oder Notizen in Echtzeit gefiltert werden.

## Vollständigkeitsprüfung

Neben der Kreistabelle zeigt ein Badge, ob die Show vollständig ist:

- **Grüner Haken** – alle Kreise vollständig ausgefüllt
- **Gelbes Warnsymbol mit Zahl** – Anzahl der Kreise mit fehlenden Angaben

Ein Klick auf das Badge öffnet die Aufschlüsselung nach fehlender Angabe (kein Gerät, keine Bühnenposition, keine Adresse). Klick auf eine Zeile filtert die Kreistabelle auf genau diese Kreise; ein **×** neben dem aktiven Filter setzt ihn zurück.

## Tastaturkürzel

| Aktion | Kürzel |
|--------|--------|
| Rückgängig | ⌘Z (Mac) / Ctrl+Z (Win) |
| Wiederholen | ⌘⇧Z (Mac) / Ctrl+Y (Win) |
