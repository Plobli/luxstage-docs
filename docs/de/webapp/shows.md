# Shows

## Shows-Übersicht

Die Startseite zeigt alle vorhandenen Shows als sortierbare Liste. Jede Zeile enthält:

- **Name** – Showname, z. B. „Hamlet"
- **Stand** – Vorstellungsdatum, z. B. „30.04.2026"
- **Spielzeit** – z. B. „25/26" (ab Bildschirmbreite lg sichtbar)
- **Bearbeitung** – E-Mail-Adresse der letzten bearbeitenden Person
- **Archivieren-Button** – erscheint beim Überfahren der Zeile rechts

Über den Spaltenüberschriften (Name, Stand, Spielzeit, Bearbeitung) lässt sich die Liste sortieren. Standardmäßig ist die Liste nach **„Stand" absteigend** sortiert (neueste zuerst), nicht alphabetisch. Ein Pfeil (↑/↓) an der Spaltenüberschrift zeigt die aktive Sortierrichtung; erneutes Klicken kehrt sie um. Bei „Name" ist die Vorbelegung aufsteigend, bei allen anderen Spalten absteigend.

Shows werden nach Spielort gruppiert angezeigt, mit dem Spielort-Namen als Überschrift. Shows ohne zugewiesenen Spielort erscheinen unter „—". Die Sortierung wirkt **innerhalb** der Spielort-Gruppen — die Gruppen selbst stehen immer alphabetisch, unabhängig von der gewählten Sortierung.

::: tip Spalten je nach Fensterbreite
„Spielzeit" erscheint erst ab mittlerer Bildschirmbreite, „Stand" und „Bearbeitung" erst ab kleiner Bildschirmbreite. Auf schmalen Bildschirmen (z. B. Tablet im Hochformat) sind entsprechend weniger Spalten sichtbar.
:::

## Neue Show erstellen

Der **„Neue Show"**-Button (unten rechts) öffnet ein Dropdown-Menü mit zwei Optionen:

- **Neue Show (Quick)** — öffnet einen einfachen Dialog zur schnellen Erfassung von Name und Datum; keine Vorlagen oder Detaileinstellungen
- **Assistent** — startet einen mehrstufigen Assistenten mit erweiterten Optionen (siehe unten)

### Assistent (mehrstufig)

Je nach Auswahl durchläuft der Assistent bis zu sechs Schritte:

1. **Vorlage** – bestehende Spielort-Vorlage auswählen oder „Keine Vorlage"
2. **Name & Datum** – Name, Datum, optional Spielzeit (z. B. „25/26")
3. **Bereiche** – Gassentürme und/oder Zugstangen aktivieren; bei gewählter Vorlage zusätzlich deren Abschnitte einzeln auswählen und optional die Kreisliste der Vorlage übernehmen
4. **Obermaschinerie** (nur wenn Vorlage + Bereich „Zugstangen" aktiv und die Vorlage welche enthält) – einzelne Elemente der Vorlage auswählen
5. **Gassentürme** (nur wenn Vorlage + Bereich „Gassentürme" aktiv und die Vorlage welche enthält) – einzelne Türme der Vorlage auswählen

6. **Kreise** – die Startfrage „Wie kommen die Kreise herein?“ (siehe unten). Dieser Schritt entfällt, wenn du eine Vorlage mit Kreisen übernimmst.

Zum Abschluss zeigt eine **Zusammenfassung** alle gewählten Werte; Klick auf **„Show erstellen"** legt die Show an.

::: tip Hinweis
Wird eine Vorlage ausgewählt, übernimmt die neue Show wahlweise die Kreisstruktur, die ausgewählten Abschnitte, Gassentürme und Zugstangen des gewählten Spielorts.
:::

### Wie kommen die Kreise herein?

Im Schritt **„Kreise“** wählst du, woher die Kreise deiner neuen Show kommen. Es gibt vier Wege:

1. **Vom Pult holen** – LuxStage liest die Kreise direkt aus dem Lichtpult. Das geht nur in der [Desktop-App](/de/webapp/desktop-app). In der Web-App im Browser ist der Weg grau, dort steht: „Dafür brauchst du die Desktop-App.“
2. **Eos-Datei importieren** – du hast eine Datei (CSV) vom Pult. Klicke auf **„Datei wählen“** und such die Datei aus. Mehr dazu unter [Aus Eos importieren](/de/webapp/import-eos).
3. **Selbst eintragen** – du trägst die Kreise von Hand ein. Die Kreisliste ist zuerst leer.
4. **Foto vom Vordruck lesen** – klein ganz unten und als **Beta** gekennzeichnet. Du wählst ein Foto deiner ausgefüllten Kreisliste. Mehr dazu unter [Kreisliste scannen](/de/webapp/scan-kreisliste).

Du kannst Kreise später jederzeit noch holen oder ergänzen, über **„Importieren“** in der Show.

Nach **„Show erstellen“** läuft der gewählte Weg mit den bekannten Dialogen. Du siehst zuerst eine Vorschau und bestätigst sie. Danach kommt der Schritt **„Prüfen“**. Er zeigt, wie viele **Kreise** und wie viele **verschiedene Geräte** jetzt in deiner Show stehen.

- **„Passt“** schließt den Dialog.
- **„Rückgängig“** nimmt den Import zurück. Die Kreisliste ist dann wieder so wie davor.

## Show öffnen

Einfach auf die gewünschte Show-Zeile klicken. Die Show öffnet sich standardmäßig im **Kreise**-Tab, merkt sich aber den zuletzt bearbeiteten Tab — wurde die Show zuletzt z. B. im Gassentürme- oder Obermaschinerie-Tab bearbeitet, öffnet sie sich beim nächsten Mal dort wieder.

## Show-Metadaten nachträglich ändern

In der geöffneten Show lässt sich der **Showname** direkt anklicken und bearbeiten. Ein Klick auf das **Datum** (bzw. auf „Info", falls noch kein Datum gesetzt ist) neben dem Namen öffnet einen Dialog zum Bearbeiten von Datum und Spielzeit.

## Show archivieren

Beim Überfahren der Show-Zeile erscheint rechts ein **Archivieren-Symbol**. Nach Bestätigung verschwindet die Show von der Startseite und erscheint im **Archiv**.

::: warning Achtung
Das Archivieren kann im Archiv rückgängig gemacht werden. Eine endgültige Löschung ist über den Archiv-Bereich möglich.
:::

## Demo-Show

Jedes neue Team bekommt eine **Demo-Show** zum Ausprobieren. Sie steht in der Show-Liste mit der Markierung **„Demo"** und zeigt Kreisliste, Gassentürme, Zugstangen, Standorte und Grundriss mit Beispieldaten.

- **Ändern erlaubt** – du kannst in der Demo-Show alles ausprobieren.
- **Ohne Notizen ausblenden** – in der Demo-Show ist dieser Filter zu Beginn eingeschaltet, die Kreisliste zeigt also nur Kreise mit Notiz. Mit dem Knopf in der Aktionszeile schaltest du ihn aus. **„Zurücksetzen"** schaltet ihn wieder ein. In anderen Shows ist der Filter davon unabhängig.
- **Zurücksetzen** – im Hinweisband oben in der Show stellt **„Zurücksetzen"** den Ausgangszustand wieder her. Das gilt für alle im Team.
- **Ausblenden** – beim Überfahren der Zeile blendet das Augen-Symbol die Demo-Show **nur für dich** aus. Über **Hilfe → „Demo-Show einblenden"** kommt sie zurück.
- **Nicht löschbar** – die Demo-Show lässt sich weder archivieren noch löschen, auch nicht als Administrator.

::: tip Teams ohne Demo-Show
Teams, die vor Einführung der Demo-Show angelegt wurden, bekommen sie über **Hilfe → „Demo-Show einblenden"**.
:::

## Tour durch die Demo-Show

Neue Konten bekommen beim ersten Start die Demo-Show mit einer kurzen **Tour** angeboten. Bestehende Konten finden die Tour jederzeit unter **Hilfe**. Du kannst sie ansehen oder mit **„Selbst umsehen"** überspringen. Die Tour startet nie von allein.

Ein kleines Fenster erscheint direkt an der jeweiligen Stelle, oben zeigt eine Punkteleiste, wie viele Schritte noch kommen. Die Tour zeigt den Weg zur eigenen Show in sechs Stationen:

1. **Show anlegen** – hier startest du später deine eigene Show.
2. **Kreise übernehmen** – in der Demo sind die Kreise schon da. Bei dir kommen sie vom Pult oder aus einer Datei.
3. **Kreise bearbeiten** – die Tour geht Spalte für Spalte durch: **Kreisnummer und Adresse**, **Color**, **Anzahl und Gerät**, **Notizen**, der Knopf **„Ohne Notizen ausblenden"**, **Prio** und **Position**.
4. **Bereiche der Show** – hier wechselst du zwischen Aufbaunotizen, Gassentürmen, Obermaschinerie, Fotos, Zeichnung und den weiteren Bereichen.
5. **Mit dem Handy einleuchten** – das Handy verbindest du mit einem Code. In der Demo ist das nur eine Vorschau.
6. **Liste drucken** – die Kreisliste als PDF.

Ein pulsierender Leuchtpunkt zeigt auf die Stelle der aktuellen Station, die Pfeilspitze des Tour-Fensters weist darauf. Du kannst jederzeit selbst klicken. **„Weiter"** und **„Zurück"** wechseln die Station, **„Beenden"** schließt die Tour.

- **Nach einer Unterbrechung** macht die Tour dort weiter, wo du aufgehört hast. Der Stand gehört zu deinem Benutzerkonto.
- **Noch einmal ansehen** – über **Hilfe → „Tour noch einmal ansehen"** (auf der Show-Liste). In der Desktop-App findest du den Befehl auch in der Menüleiste unter **Hilfe**. Ist die Demo-Show ausgeblendet, blendet dieser Eintrag sie wieder ein.
- **Am Ende** fragt LuxStage, ob du eine eigene Show anlegen oder noch etwas stöbern möchtest. Ohne Konto führt **„Eigene Show anlegen"** zur Registrierung.
- Die Tour gibt es in der Web-App und in der Desktop-App ab einer Fensterbreite von 768 Pixeln, nicht in den Smartphone-Apps.

## Demo ohne Konto

Die Web-App lässt sich unter **demo.luxstage.app** ohne Konto ausprobieren, auch in der Desktop-App über **„Demo ansehen"**. Jede Person bekommt eine eigene Kopie der Demo-Show. Die Demo braucht eine Internetverbindung.

- Die Kopie wird nach **20 Minuten ohne Aktivität** gelöscht. Danach bietet die Demo einen Neustart an.
- **Zurücksetzen** stellt den Ausgangszustand jederzeit wieder her.
- Der Einleuchtplan lässt sich als **PDF-Vorschau** ansehen, aber nicht herunterladen. Auch der CSV-Export fehlt.
- Nicht verfügbar sind außerdem Fotos hochladen, Import, Einstellungen, Team, Benutzer und Abrechnung.
