# iOS-App – Übersicht

Die native LuxStage-App für iPhone und iPad ist in SwiftUI geschrieben und für Touch-Bedienung optimiert — ob am Mischpult oder auf der Bühne.

## Aufbau der App

Die App ist in zwei Ebenen gegliedert:

**Globale Tabs** (sichtbar auf der Shows-Übersicht):

| Tab | Funktion |
|-----|----------|
| **Shows** | Liste aller Shows, nach Spielort gruppiert |
| **OSC** | Direkte EOS-Steuerung ohne aktive Show |
| **Cues** | Cue-Liste live vom Pult |
| **Einstellungen** | Team, Sprache, Remote-Verbindung, Diagnose |

**Show-Tabs** (sichtbar innerhalb einer geöffneten Show):

| Tab | Funktion |
|-----|----------|
| **Aufbau** | Aufbaunotizen der Show; über den Bereiche-Button Zugriff auf Gassentürme, Obermaschinerie, Fotos, Zeichnung und weitere Bereiche |
| **Einleuchten** | Kreisplan zum Fokussieren der Scheinwerfer |
| **OSC** | EOS-Fernsteuerung (Numpad, Playback, Fader, ML) |
| **Suche** | Suche nach Kreisen, Gassentürmen, Obermaschinerie, Standorten, Abschnitten und Fotos (Name, Notiz oder Kreisnummer). Ein Tipp auf einen Kreis zeigt Gerät, Adresse, Position, Farbe und Notizen; von dort springst du in die Lichtliste |

## Nächste Schritte

- [Shows](./shows) — Shows öffnen und anlegen
- [Aufbau](./aufbau) — Aufbaunotizen und Bereiche-Menü
- [Bereiche](./bereiche) — Gassentürme, Obermaschinerie, Fotos, Zeichnung
- [Einleuchten](./einleuchten) — Scheinwerfer fokussieren
- [OSC](./osc) — EOS-Konsole fernsteuern
- [Cues](./cues) — Cue-Liste live vom Pult
- [Einstellungen](./einstellungen) — Team, Remote-Verbindung und Diagnose
