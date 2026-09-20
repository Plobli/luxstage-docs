# Kreise

Der **Kreise**-Tab (in der App-Sidebar als **„Kreisliste"** bezeichnet) ist die Hauptansicht einer Show und zeigt den vollständigen Kreisplan.

::: tip Inline-Hilfe in der App
Neben den Spaltenüberschriften der Kreistabelle und im Setup-Bereich zeigen kleine Hilfe-Icons Kurzerklärungen zu den jeweiligen Feldern direkt in der App.
:::

## Live-Zusammenarbeit (Presence)

Hat eine Show mindestens eine verbundene Person, erscheinen oben in der Show-Leiste kleine Avatare (Initiale) für jede angemeldete Person. Rein informativ, keine Sperre.

- Tooltip beim Überfahren zeigt Name und verbundene Geräte (z. B. „ios, web")

Wer schreiben darf, regelt separat die Bearbeitungssperre (Schreib-Lock), nicht die Presence-Anzeige. Änderungen anderer Nutzer erscheinen in Echtzeit, ohne Neuladen der Seite.

## Bearbeitungssperre (Lock) und Übernahme

Bearbeitet eine Person die Show, wird sie für alle anderen gesperrt: Ein Badge zeigt „Wird bearbeitet von {Person}", die Bearbeitung ist blockiert.

Andere Nutzer können die Übernahme anfragen:

- Die anfragende Person sieht „Übernahme angefragt — warte auf Freigabe"
- Die aktuell bearbeitende Person sieht einen Dialog „Übernahme angefragt" mit den Optionen **„Freigeben"** und **„Ignorieren"**
- Reagiert die bearbeitende Person nicht, läuft ein Countdown („Übernahme in Xs erzwingbar"); danach kann die anfragende Person die Sperre mit **„Jetzt übernehmen"** erzwingen

## Konflikt beim Speichern

Ändern zwei Personen (z. B. durch parallele Sitzungen oder abgelaufene Sperre) gleichzeitig dieselbe Kreisliste oder denselben Abschnitt, erscheint beim Speichern der Dialog **„Jemand anders hat gespeichert"**: Während der Bearbeitung hat eine andere Person bereits gespeichert, die eigenen Änderungen wurden noch nicht übernommen. Zur Auswahl stehen:

- **„Anderen Stand übernehmen"** – verwirft die eigenen Änderungen und lädt den gespeicherten Stand
- **„Trotzdem überschreiben"** – überschreibt den gespeicherten Stand mit den eigenen Änderungen

## Aufbau des Kreisplans

Die Tabelle hat folgende Spalten:

| Spalte | Bedeutung |
|--------|-----------|
| **KREIS** | Kreisnummer, reine Zahl, z. B. „1" |
| **DMX** | Universum/Adresse, z. B. „1/121" |
| **COLOR** | Farbfilter (Gel-Code), z. B. „L201/R371" oder „RGB", „variable" |
| **ANZ.** | Anzahl identischer Geräte an dieser Bühnenposition |
| **GERÄT** | Leuchtenbezeichnung, z. B. „ETC Source Four 26°" |
| **NOTIZEN** | Freitext-Notiz, z. B. „Key light stage left, narrow spot" |
| **ZUWEISEN** | Button zum Zuweisen eines Einbauorts (siehe unten) |

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

::: details DMX-Adresse wird automatisch normalisiert
Beim Verlassen des Adressfelds wird die Eingabe automatisch ins Format „Universum/Adresse" gebracht, z. B. wird aus „129" automatisch „1/129" und aus „1/1" wird „1/001". Reine Zahlen über 512 werden dabei als durchlaufende Adresse über mehrere Universen interpretiert (z. B. „515" → „2/003").
:::

## Kreis-Status umschalten

Die **Kreisnummer** erscheint in drei Farben:

- **Weiß** – ohne Notiz und ohne Einbauort
- **Grün** – Notiz vorhanden oder einem Einbauort (Beleuchtungsgestell-Slot, Zugstange, oder Zeichnung) zugewiesen
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

- **In der Zeichnung platzieren** – öffnet die [Zeichnung](./grundriss) und platziert den Kreis dort
- **Beleuchtungsgestell-Slot zuweisen** – öffnet [Setup — Beleuchtungsgestelle](./setup-gestelle) zur Zuweisung an ein Gestell
- **Zugstange zuweisen** – öffnet [Setup — Zugstangen](./setup-zugstangen) zur Platzierung auf einer Zugstange

Ist der Kreis bereits einem Gestell-Slot, einer Zugstange oder einem Ort in der Zeichnung zugewiesen, wird der Einbauort zusätzlich als kleines Badge unterhalb der Notiz angezeigt.

**Bühnenpositionen** (z. B. „FOH BAR LEFT", „OVERHEAD BAR 1") können nur umbenannt, aber nicht gelöscht werden.

::: tip Warnung bei Duplikaten
Vergibst du eine DMX-Adresse oder Kreisnummer doppelt, warnt die Tabelle mit „Doppelte DMX-Adresse!" bzw. „Doppelte Kreisnummer!".
:::

## Reihenfolge ändern (Drag & Drop)

Per **Drag & Drop** am ⠿-Handle links können Kreise innerhalb einer Bühnenposition neu angeordnet werden.

## Bühnenposition umbenennen

Beim Hovern über eine Bühnenpositions-Überschrift erscheint der Button **„Bühnenposition umbenennen"** – klicken und neuen Namen eingeben.

## Suche

Im Suchfeld oben rechts (**„In Kreisen suchen …"**) können Kreise, Geräte oder Notizen in Echtzeit gefiltert werden.

## Vollständigkeitsprüfung

Neben der Kreistabelle zeigt ein Badge, ob die Show vollständig ist:

- **Grüner Haken** – alle Kreise vollständig ausgefüllt
- **Gelbes Warnsymbol mit Zahl** – Anzahl der Kreise mit fehlenden Angaben

Ein Klick auf das Badge öffnet die Aufschlüsselung nach fehlender Angabe (kein Gerät, keine Bühnenposition, keine Adresse, Kreise ohne Notiz). Klick auf eine Zeile filtert die Kreistabelle auf genau diese Kreise; ein **×** neben dem aktiven Filter setzt ihn zurück.

## Tastaturkürzel

| Aktion | Kürzel |
|--------|--------|
| Rückgängig | ⌘Z (Mac) / Ctrl+Z (Win) |
| Wiederholen | ⌘⇧Z (Mac) / Ctrl+Y (Win) |
