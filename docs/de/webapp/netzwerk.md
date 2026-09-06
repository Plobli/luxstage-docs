# Netzwerk

Der **Netzwerk**-Tab dokumentiert die IT-Infrastruktur einer Spielstätte — Netzwerkdosen, Geräte, Switches und ihre Verkabelung — unabhängig von Shows und Spielort-Vorlagen.

## Elemente

Ein Element ist eine der drei Grundbausteine der Netzwerkdokumentation:

| Typ | Bedeutung |
|-----|-----------|
| **Dose** | Eine Netzwerkdose (Anschlusspunkt in der Wand/im Boden) |
| **Gerät** | Ein Endgerät (z. B. Access Point, Kamera, PC) |
| **Switch** | Ein Netzwerk-Switch mit einer festen Anzahl Ports |

Elemente werden über den Button **„+ Element hinzufügen"** unterhalb der Elemente-Tabelle angelegt (Typ auswählen). Jedes Element hat:

- **Typ** — Dose, Gerät oder Switch (per Dropdown änderbar)
- **Bezeichnung** — Freitext-Name
- **Ort** — einem Raum zuweisen oder „Kein Ort" lassen
- **Ports** (nur Switches) — Anzahl der Switch-Ports
- **Hauptswitch** (nur Switches) — Checkbox zur Kennzeichnung des zentralen Switches

Ein Element wird über das Papierkorb-Symbol in der jeweiligen Zeile gelöscht. Sind für das Element noch Verbindungen hinterlegt, warnt ein Dialog, dass diese ebenfalls entfernt werden.

## Räume

Elemente lassen sich einem **Ort** (Raum) zuweisen — die Elemente-Tabelle gruppiert automatisch nach Ort, mit der Anzahl der Elemente je Gruppe. Jede Gruppe lässt sich per Klick auf die Kopfzeile ein- und ausklappen. Elemente ohne Ort erscheinen in der Gruppe „Kein Ort".

Ein neuer Ort wird direkt im Orts-Dropdown eines Elements über **„+ Neuer Ort…"** angelegt.

## Suche

Das Suchfeld oben rechts in der Elemente-Tabelle filtert die Liste in Echtzeit.

## Verbindungen

Verbindungen bilden die Verkabelung zwischen zwei Elementen ab.

### Switches als Port-Grid

Für jeden Switch zeigt die Ansicht ein Grid mit einem Feld pro Port (Anzahl gemäß hinterlegter Portzahl). Ein Port zeigt:

- Ein Dropdown zur Auswahl, welches Element an diesem Port angeschlossen ist (oder „Frei")
- Zusätzlich ein Portfeld, falls das Gegenüber ebenfalls ein Switch ist — so lässt sich die Verbindung zweier Switches auf Port-Ebene in beide Richtungen nachvollziehen

Oberhalb jedes Grids zeigt ein Badge die Belegung, z. B. „(6/24)". Switches ohne hinterlegte Portzahl zeigen stattdessen den Hinweis „Keine Portanzahl hinterlegt."

### Sonstige Verbindungen

Verbindungen, an denen kein Switch beteiligt ist (z. B. Gerät direkt an Gerät), erscheinen zusätzlich in einer eigenen Tabelle mit den Spalten „Von" und „Zu". Neue Verbindungen werden über **„+ Verbindung hinzufügen"** angelegt; solange nicht beide Enden gewählt sind, bleibt der Eintrag ein Entwurf (farblich hervorgehoben) und wird erst mit vollständiger Auswahl gespeichert.

::: tip Nur gültige Kombinationen wählbar
Beim Zuweisen eines Verbindungspartners werden nur Elemente angeboten, die laut Elementtyp überhaupt sinnvoll miteinander verbunden werden können. Hat ein Ziel bereits die maximale Anzahl Verbindungen erreicht, fragt ein Dialog, ob die älteste Verbindung ersetzt werden soll.
:::

## Topologie (interaktiver Graph)

Oberhalb der Elemente- und Verbindungstabellen zeigt die Topologie-Ansicht alle Elemente als frei verschiebbare Knoten, verbunden durch Linien (Kabel) entsprechend der hinterlegten Verbindungen.

- **Verbindung ziehen** — direkt im Graph von einem Anschlusspunkt zu einem anderen ziehen, um eine neue Verbindung anzulegen
- **Verbindung umhängen** — eine bestehende Linie am Endpunkt greifen und auf ein anderes Element ziehen
- **Element/Verbindung löschen** — Auswählen und Entf/Backspace drücken
- **Automatisch anordnen** — ordnet neue, noch nicht platzierte Elemente automatisch an (Switches als Ausgangspunkt); einmal selbst verschobene Elemente bleiben an ihrer Position
- **Ansicht speichern / wiederherstellen** — die aktuelle Anordnung der Knoten sichern bzw. auf den zuletzt gespeicherten Stand zurücksetzen
- **Vollbild** — Topologie-Karte im Vollbildmodus anzeigen (auch per Esc wieder verlassen)

Sind noch keine Elemente angelegt, zeigt die Topologie den Hinweis „Noch keine Elemente angelegt."

## Live-Zusammenarbeit

Wie bei Shows wird die Netzwerkdokumentation gesperrt, sobald eine andere Person aktiv bearbeitet — ein Hinweis zeigt, wer gerade sperrt.

## Rückgängig / Wiederholen

Änderungen an Elementen und Verbindungen lassen sich über die Buttons oben rechts (bzw. die üblichen Tastaturkürzel) rückgängig machen und wiederholen.

## PDF-Export

Über den Button **„PDF exportieren"** oben rechts lässt sich die vollständige Netzwerkdokumentation als PDF herunterladen.
