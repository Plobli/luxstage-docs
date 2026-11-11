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
| **2. FOLIE** | Optionale zweite Folie. Einblenden über den Umschalter 1×/2× im Spaltenkopf von COLOR (gilt für die ganze Show, auch in den Apps); sobald ein Kreis eine 2. Folie hat, bleibt die Spalte sichtbar |
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
| **Gel** | Klicken → Dropdown mit allen Farben erscheint, eigene Farben ganz oben (z. B. „L201 / R371 Full C.T. Blue"). Frost und Diffusion erscheinen schraffiert. Die Liste pflegst du unter [Farben verwalten](/de/webapp/farben). Zusätzlich wählbar: **„No Color"** (kein Farbfilter) oder **Freitext** für eigene Angaben (z. B. „R02" oder „warm weiß") |
| **Gerät** | Klicken → Gerätebezeichnung eingeben |
| **Notizen** | Klicken → Freitext eingeben |

::: details DMX-Adresse wird automatisch normalisiert
Beim Verlassen des Adressfelds wird die Eingabe automatisch ins Format „Universum/Adresse" gebracht, z. B. wird aus „129" automatisch „1/129" und aus „1/1" wird „1/001". Reine Zahlen über 512 werden dabei als durchlaufende Adresse über mehrere Universen interpretiert (z. B. „515" → „2/003").
:::

## Persönliche Anmerkung

Zu jeder Kreisnotiz kannst du eine eigene Anmerkung schreiben. Nur du siehst sie. Die Notiz fürs Team bleibt unverändert. Die Anmerkung steht darunter in Violett und Kursiv.

- **Anlegen:** In der Zeile auf **Persönliche Anmerkung hinzufügen** klicken, Text eingeben.
- **Löschen:** Text entfernen, Feld verlassen.
- Nicht sichtbar für andere, im Versionsverlauf, in PDF-/CSV-Export und in Vorlagen.
- Kein Live-Sync, keine Show-Sperre.

## Notiz als Hinweis markieren

Manche Notizen sind eine Aufgabe, kein Einleuchten, zum Beispiel „Wegdrehen“. Klicke dafür rechts in der Notiz auf das **Werkzeug-Symbol**. Der Kreis ist dann ein Hinweis, das Symbol wird orange. Nochmal klicken hebt die Markierung auf.

- In den Smartphone-Apps hat ein Hinweis-Kreis kein Ein/Aus und zählt nicht im Fortschritt.
- Direkt aufeinanderfolgende Hinweise mit gleichem Text erscheinen dort als eine Zeile mit einem Haken für alle.
- Ohne Notiztext gibt es keinen Hinweis: Wird der Text gelöscht, fällt die Markierung weg.

## Kreis-Status umschalten

Die **Kreisnummer** erscheint in drei Farben:

- **Weiß** – ohne Notiz und ohne Einbauort
- **Grün** – Notiz vorhanden oder einem Einbauort (Gassenturm-Slot, Zugstange, oder Zeichnung) zugewiesen
- **Gelb** – in der Show aktiv (z. B. nach EOS-Import), aber weder Notiz noch Einbauort vorhanden

Dieselbe Legende steht auch als Inline-Hilfe (Hilfe-Icon) neben der Kreistabelle in der App.

## EOS-Import: gelesene Felder

Der Import einer EOS-CSV übernimmt pro Kreis:

- **Kreisnummer, Adresse, Gerät** (Hersteller und Typ) in die Kreisliste
- **Aktiv-Status** (Intensität > 0) und **Moving Lights** (Pan/Tilt)
- **Alle weiteren Patch-Felder**, soweit gefüllt: Label, Notes, Text1–Text10, Gel, Gobo, Dimmerkurve, Position und Ausrichtung

Das gilt für „Eos-CSV“ und „CSV“. Der Pult-Sync (Desktop-App) übernimmt Label, Notes, Gel und Text1–10; Position und Ausrichtung folgen später. Eos-CSV und CSV (Eos-Export wird erkannt; ANSI-Dateien mit Umlauten werden korrekt gelesen). Die Zusatzfelder erscheinen als Tooltip an der Geräte-Zelle. Die Kreissuche findet auch Texte darin. Bei jedem Import gilt der aktuelle Pultstand.

**Gel vom Pult:** Das Pult-Feld „Gel“ füllt die Spalte **Gel** der Kreisliste (leere Felder füllen oder bestehende überschreiben, wie bei Notizen).

**Pult-Feld als Notiz:** Viele Teams nutzen für Focus-Notizen unterschiedliche Felder (Label, Notes oder einen Text). Im Eos-Import-Dialog und im Pult-Sync wählst du, welche Pult-Felder in die Einleuchtnotiz übernommen werden (Standard: keins). Mehrere Felder werden in der Reihenfolge der Auswahl mit „ · “ verbunden, leere und doppelte Werte entfallen. Je Feld wählst du „Notiz“ oder „Tag“: Tag-Felder werden als eigene Tags am Kreis gespeichert und in der Einleuchtnotiz am Ende als #tag angezeigt, mehrere hintereinander (z. B. „#Turm #Schauspiel“). Neue Tags schreibst du einfach in die Einleuchtnotiz (z. B. „Person Bühne hinten #Turm“); sobald du danach ein Leerzeichen tippst (oder das Feld verlässt), wird „#Turm“ zum Tag und steht am Ende der Zelle. Mit dem Kreuz entfernst du ihn wieder; die Suche findet sie. Die Wahl gilt für die Show. Je Import legst du fest, ob nur leere Notizen gefüllt oder vorhandene überschrieben werden. Leere Pult-Felder löschen nie eine Notiz.

## Mehrere Kreise gemeinsam ändern

Ein Klick auf eine Zeile markiert sie und blendet die Leiste ein. Mit **Shift** markierst du mehrere Zeilen am Stück, mit **Cmd/Strg** einzelne Zeilen dazu, wie in Excel. Alternativ: Checkbox links in der Zeile (oder Maus-Drag über die Checkbox-Spalte). Die Checkbox im Tabellenkopf wählt alle aus. Eine Leiste zeigt „{n} ausgewählt" und bietet:

- **Position**, **Gerät**, **Gel**, **Prio** – Wert für alle gewählten Kreise setzen
- **Notiz** – bestehende Notizen **ersetzen** oder den Text **anhängen**
- **Leeren** – entfernt Notiz, Gerät und Gel; Kreisnummer und DMX-Adresse bleiben
- **Löschen** – entfernt die Kreise vollständig (nicht rückgängig zu machen)
- **Auswahl aufheben**

## Priorität (Prio)

Die Spalte **Prio** legt die Reihenfolge beim Einleuchten fest — niedrigere Zahl zuerst. Die Prio erscheint als farbiges Badge, auch im PDF-Export und in den Apps.

## Sortieren und ausblenden

Ein Klick auf eine Spaltenüberschrift sortiert die Tabelle (erneut klicken: Richtung wechseln). Über der Tabelle zeigt „Sortiert nach: …" die aktive Sortierung, **Zurücksetzen** stellt die Ausgangsreihenfolge wieder her. Die Option **„Kreise ohne Notiz ausblenden"** blendet alle Kreise ohne Notiz aus.

## Kreis hinzufügen

Unterhalb jeder Bühnenposition befindet sich der Button **„+ Kreis hinzufügen"**. Ein Klick fügt einen neuen leeren Kreis zur jeweiligen Bühnenposition hinzu.

## Kreis löschen oder leeren

Den Kreis anklicken (aktivieren), dann auf das **×**-Symbol rechts in der Zeile klicken. Ein Dialog bietet zwei Optionen:

- **Kreis leeren** – entfernt nur Notiz und Gel, die Zeile bleibt bestehen
- **Zeile löschen** – entfernt den Kreis vollständig

## Kreis einem Einbauort zuweisen

Bei Hover über eine Kreiszeile erscheint rechts (vor dem Löschen-Button) der Button **„Zuweisen"** mit drei Optionen:

- **In der Zeichnung platzieren** – öffnet die [Zeichnung](./grundriss) und platziert den Kreis dort
- **Gassenturm-Slot zuweisen** – öffnet [Setup — Gassentürme](./setup-gestelle) zur Zuweisung an einen Turm
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

Das Suchfeld gilt auch in den Tabs **Gassentürme**, **Obermaschinerie**, **Standorte** und **Fotos**. Du findest Elemente nach Name, Notiz oder zugeordneter Kreisnummer. Mehrere Wörter müssen alle passen. Aufbaunotizen, Raum und Zeichnung sind nicht durchsuchbar.

## Nach Chips filtern

Über **Filter** in der oberen Leiste filterst du die Kreisliste nach Gassentürmen, Obermaschinerie, Kulissen und Standorten. Mehrere Einträge sind möglich: Innerhalb einer Art zählt „oder", zwischen Arten „und". Ein Klick auf einen Chip in der Liste setzt denselben Filter. Gewählte Einträge zeigen einen Ring und ein Häkchen, die Zahl neben **Filter** nennt die aktive Auswahl. Der Filter gilt nur in der Web-App.

## Vollständigkeitsprüfung

Neben der Kreistabelle zeigt ein Badge, ob die Show vollständig ist:

- **Grüner Haken** – alle Kreise vollständig ausgefüllt
- **Gelbes Warnsymbol mit Zahl** – Anzahl der Kreise mit fehlenden Angaben

Ein Klick auf das Badge öffnet die Aufschlüsselung nach fehlender Angabe (kein Gerät, keine Bühnenposition, keine Adresse, Kreise ohne Notiz). Klick auf eine Zeile filtert die Kreistabelle auf genau diese Kreise; ein **×** neben dem aktiven Filter setzt ihn zurück.

## Kreisgruppen

Mit **Gruppen** in der Kopfleiste fasst du Kreise zu benannten Gruppen zusammen, z. B. „Rücklicht“ mit den Kreisen `137-148`. Optional trägst du die Gruppennummer am Pult ein.

- Kreise gibst du als Bereich oder Liste ein (`137-148, 150`).
- Ein Kreis kann in mehreren Gruppen sein.
- Die Liste zeigt eine Zeile pro Gruppe; zum Ändern auf die Zeile klicken. Ein Kreis in mehreren Gruppen steht in den Apps unter der kleinsten seiner Gruppen. Die anderen erscheinen als Chips hinter dem Kreis.
- **Aus Pult importieren** (nur Desktop-App): holt die Gruppen per OSC aus Eos. Gruppen mit gleicher Pult-Nummer oder gleichem Namen werden aktualisiert, neue kommen dazu. Gespeichert wird erst mit „Speichern“.
- Gruppen erscheinen als Chips in der Kreistabelle und im **Filter**. Ein Klick filtert die Tabelle auf die Gruppe.

## Tastaturkürzel

| Aktion | Kürzel |
|--------|--------|
| Rückgängig | ⌘Z (Mac) / Ctrl+Z (Win) |
| Wiederholen | ⌘⇧Z (Mac) / Ctrl+Y (Win) |
