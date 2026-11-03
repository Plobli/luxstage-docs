# Kreisliste (iOS)

Der **Kreisliste**-Tab (früher „Einleuchten") ist die zentrale Fokussier-Ansicht der Show. Er zeigt die Kreise der Produktion nach Platzierung sortiert: erst **Gassentürme** (nach Slot), dann **Standorte**, dann **Obermaschinerie** (nach Position auf dem Zug), zuletzt nicht platzierte Kreise, gruppiert nach **Bühnenposition** (z. B. „FOH SL Slot"). Das **Stapel-Symbol** in der Kreisliste schaltet auf Sortierung nach Bühnenposition und Nummer um, ebenso **Nach Nummer sortieren** in den [Einstellungen](./einstellungen#kreisliste). Der Umschalter **Mit Notiz / Alle** wählt, ob nur Kreise mit Notiz oder alle erscheinen. Kreise bearbeitest du per Lang-Drücken, siehe [Bearbeiten](./bearbeiten).

## Kreisanzeige

<img src="/img/ios/einleuchten-kanalliste.png" alt="Kreisliste" class="ios-screenshot">

Jeder Kreis wird als Karte mit folgenden Elementen dargestellt:

| Element | Bedeutung |
|---------|-----------|
| **Große Kreisnummer** (z. B. `001`) | Wird rot, sobald der Kreis als fokussiert markiert ist |
| **Name und Gerät** | z. B. „Person Stage Left · 1/1 · ETC Source Four 26°" |
| **Fokus-Kreis** (links) | Tippen → Kreis als fokussiert markieren (roter Haken) |
| **OSC-Toggle** (rechts) | Kreis über OSC auf Full schalten; aktiv = grüner Toggle, Karte rosa hinterlegt |

## Wo hängt der Kreis?

Unter jedem Kreis zeigen **Pillen**, wo er aufgebaut ist, z. B. „Gassenturm 1 · Slot 3“, eine Batten der Obermaschinerie oder ein Standort. Kreise ohne Platz zeigen keine Pille. Die Pillen erscheinen in der Liste und im Kachel-Sheet.

Ein Tipp auf eine Pille öffnet einen **Schnellblick** ohne Tab-Wechsel: Bei einem Turm siehst du alle Slots mit Kreisnummer, bei einer Batten alle Geräte nach Position, bei einem Standort alle zugehörigen Kreise. Dein Kreis ist hervorgehoben. **Bearbeiten** öffnet den Eintrag zum Ändern.

## Fortschritt

Oben rechts zeigt der Status, wie viele Kreise bereits fokussiert wurden, z. B. `64 · 50%`.

### Hinweise

Kreise, deren Notiz du in der Web-App als **Hinweis** markiert hast (zum Beispiel „Wegdrehen“), sind keine Scheinwerfer zum Einleuchten. Sie erscheinen als schmale orange Zeile ohne Ein/Aus. Aufeinanderfolgende Hinweise mit gleichem Text sind eine Zeile, z. B. „136–147 · 12“. Ein Tipp hakt alle ab. Im Fortschritt zählen sie nicht. Daneben steht eine eigene Zählung mit Flagge, z. B. `⚑ 0/1`.

## Gruppen

Hast du in der Web-App Kreisgruppen angelegt, zeigt die Liste für jede Gruppe eine Karte mit Name, Kreisbereich und Zähler. Ein Kreis steht unter der ersten Gruppe, zu der er gehört; weitere Gruppen erscheinen als kleine Chips.

- **Box im Gruppenkopf** antippen → alle Kreise der Gruppe werden abgehakt (nochmal antippen: alle Häkchen weg). Die Box zeigt „teils“, wenn nur einige Kreise erledigt sind. Einzelne Kreise bleiben jederzeit einzeln abhakbar.
- **Titel oder Pfeil** antippen → Gruppe auf- oder zuklappen.
- **Chip-Leiste** über der Liste: Chip antippen filtert die Liste auf die Kreise der Gruppe, nochmal antippen hebt den Filter auf.

## Suche

Der Tab **Suche** durchsucht Kreise, Notizen und Pläne der Show.

## Workflow: Scheinwerfer einleuchten

1. Kreis in der Liste suchen oder scrollen
2. **Toggle** einschalten → die App sendet @ Full an das EOS-Pult (Karte wird farblich hinterlegt)

<img src="/img/ios/einleuchten-osc-toggle.png" alt="OSC-Toggle aktiv" class="ios-screenshot">

3. Scheinwerfer physisch fokussieren
4. **Checkmark** antippen → Kreis gilt als abgehakt (roter Haken, Nummer rot) und Scheinwerfer wird über das EOS-Pult ausgeschaltet. Alternativ, ohne den Scheinwerfer als erledigt abzuhaken: Toggle ausschalten

<img src="/img/ios/einleuchten-fokussiert.png" alt="Kreis fokussiert" class="ios-screenshot">

<img src="/img/ios/einleuchten-alle-fokussiert.png" alt="Alle Kreise fokussiert" class="ios-screenshot">

5. → weiter zum nächsten Kreis

::: tip Fotos beim Fokussieren
Dem Kreis zugeordnete **Fotos** sind direkt in der Liste abrufbar — ideal zum Vergleichen der Fokusposition.
:::
