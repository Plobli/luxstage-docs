# Setup — Gassentürme

Der **Setup**-Bereich verwaltet die physische Struktur der Bühne. Diese Seite behandelt **Gassentürme** (Türme mit nummerierten Slots) — für Zugstangen siehe [Setup — Obermaschinerie](./setup-zugstangen).

::: tip Nicht zu verwechseln
Dieser Bereich ist nicht identisch mit dem „Aufbau"-Tab der iOS-App – dieser zeigt Checklisten und Freitext-Notizen aus den [Aufbaunotizen](./info).
:::

::: tip Begriff „Traverse"
Der In-App-Hilfetext nennt als Beispiel für Gassentürme auch „Traversen neben der Bühne" — gemeint sind damit seitliche Türme mit Slots wie hier beschrieben. Der eigenständige Element-Typ **„Traverse"** unter [Setup — Obermaschinerie](./setup-zugstangen) ist etwas anderes: eine frei positionierbare Stange in der Obermaschinerie.
:::

Je nach Einstellung der Show (siehe [Shows](./shows)) ist der eine, der andere oder beide Bereiche als eigener Unter-Tab im Setup-Bereich sichtbar: Gassentürme als „Gassentürme", Zugstangen als **„Obermaschinerie"**.

## Gestell anlegen

1. Klick auf **„Neuer Gassenturm"** (unten rechts)
2. Felder ausfüllen:

| Feld | Beschreibung |
|------|-------------|
| **Bezeichnung** | Name des Gestells, z. B. „Gassenturm 1" |
| **Anzahl Slots** | Wie viele Gestellplätze das Gestell hat (1–20) |

3. Klick auf **„Anlegen"**

## Kreisliste als Leiste

Neben Gassentürmen und Obermaschinerie steht rechts die **Kreisliste als Leiste** mit Gerät, Farbe und Notiz jedes Kreises. Sie bietet:

- **Suche** nach Kreisnummer oder Gerät
- **Alle / Nicht platziert** als Filter
- **Auge-Knopf** „Nur Kreise mit Notiz"
- **Filter nach Bühnenposition** mit Zähler
- **Platz-Pille** je Kreis, z. B. „Gassenturm 1 · S1, S3"

Die Liste bleibt stabil; ein Kreis lässt sich mehrfach platzieren. Die Leiste lässt sich breiter ziehen.

## Kreis einem Slot zuweisen

**Mit der Leiste:**

1. Slot oder Kreis anklicken, dann das Gegenstück. Alternativ den Kreis aus der Leiste per Drag & Drop auf den Slot ziehen.
2. Nach einem Slot springt das Ziel zum nächsten freien Slot. Ein gewählter Kreis bleibt gewählt, bis **Esc** gedrückt wird oder ein Klick außerhalb von Turm und Leiste erfolgt.
3. Fehlt ein Kreis, legt **Enter** in der Suche eine unbekannte Nummer in der Kreisliste an.

Beim Überschreiben eines belegten Slots fragt die Leiste nicht nach; **Rückgängig** gilt weiter.

**Ohne Leiste** (Vorlagen-Editor, schmale Bildschirme, eingeklappte Leiste):

1. Bei einem leeren Slot auf **„Kreis zuordnen"** klicken, bei einem belegten Slot auf das **Stift**-Symbol
2. Im Suchfeld nach Kreisnummer oder Gerät suchen
3. Kreis anklicken → wird dem Slot zugewiesen

Ist der nächste Slot noch leer, öffnet sich automatisch dessen Auswahl-Dialog. Ist ein Slot bereits belegt, erscheint vor dem Überschreiben eine Bestätigung.

## Slot leeren

Klick auf das **×**-Symbol neben einem belegten Slot.

## Slots per Drag & Drop tauschen

Am Grip-Symbol (⠿) links neben der Slot-Nummer lässt sich die Kreiszuweisung zweier Slots per Drag & Drop tauschen.

## Slot hinzufügen

Klick auf **„Slot hinzufügen"** unterhalb der Slot-Liste des Gestells.

## Gestell bearbeiten / löschen

Über die Symbole oben rechts an jeder Gestell-Karte:

- **Stift** – Bezeichnung oder Anzahl Slots ändern. Wird die Slot-Anzahl verringert, erscheint eine Warnung mit den betroffenen (ggf. belegten) Slots.
- **Papierkorb** – Gestell nach Bestätigung löschen

## Notiz pro Slot

Jeder Slot hat ein eigenes **Aufbaunotiz**-Feld (getrennt von der Notiz der Kreisliste für das Einleuchten). Text eintragen, er wird beim Verlassen des Feldes gespeichert.

## Notiz hinzufügen

Am unteren Rand jeder Gestell-Karte lässt sich per Klick auf **„+ Notiz"** ein Freitext-Kommentar hinterlegen.

## Als Vorlage speichern

Über das Lesezeichen-Symbol lässt sich ein Gestell in die Spielort-Vorlage übernehmen. Auswählbar sind dabei Grundstruktur (immer enthalten), Kreisnummer, Gerät und Farbe je Slot.

::: tip Hinweis
Gassentürme aus der Vorlage werden beim schnellen Anlegen einer Show nicht automatisch übernommen — nur über den Erstellungs-Assistenten lassen sie sich gezielt einzeln auswählen, oder nachträglich über „Aus Vorlage einfügen…" beim Anlegen eines neuen Gestells.
:::
