# Cues (iOS)

Der **Cues**-Tab zeigt die Cue-Liste live vom Pult und hebt die aktuell laufende Stimmung hervor. Darunter liegen die Playback-Tasten. So steuerst du den Ablauf und springst gezielt in jeden Cue, ohne die Ansicht zu wechseln.

## Voraussetzung

Die App muss mit der EOS verbunden sein (siehe [OSC](./osc)). Oben links wählst du die Bühne, darunter steht der Verbindungsstand. Ohne Verbindung bleibt die Liste leer und die Tasten sind ausgegraut.

## Liste

Jede Zeile zeigt Cue-Nummer und Name. Der aktive Cue ist grün hervorgehoben und mit einem Play-Symbol markiert, der nächste Cue ist orange hinterlegt. Wechselt der aktive Cue am Pult, scrollt die Liste automatisch dorthin.

Änderungen am Pult — neuer, umbenannter oder gelöschter Cue — erscheinen von selbst. Die Liste lädt nicht regelmäßig nach, das Pult meldet jede Änderung.

## In einen Cue springen

Tippe einen Cue an. Er wird lila markiert und darunter erscheint **Go to Cue X**. Erst dieser zweite Tipp löst den Sprung am Pult aus. So springst du in der Vorstellung nicht aus Versehen. **Abbrechen** oder ein erneuter Tipp auf denselben Cue hebt die Auswahl auf.

## Playback-Tasten

| Taste | Farbe | Funktion |
|-------|-------|----------|
| **Stop/Back** | Orange | Einmal tippen hält den laufenden Cue an, zweimal tippen geht zum vorigen Cue zurück (wie die Stop/Back-Taste am Pult) |
| **GO** | Grün | Nächsten Cue starten |
| **Go Time Disable** | Türkis | GO ohne Cue-Zeit (Shift+GO) |
| **Cue Out** | Rot | Direkt zu Cue Out springen |
| **Cue** | Lila | Cue-Nummer über einen Ziffernblock eingeben und hinspringen |

## Mehrere Sequenzlisten

Hat das Pult mehr als eine Sequenzliste, erscheint oben rechts neben der Überschrift ein Dropdown zur Listenauswahl. Bei nur einer Liste fehlt es. Mit mehreren Listen wirken alle Tasten (GO, Stop/Back, Go Time Disable, Cue Out) und Sprünge auf die gewählte Liste. Mit nur einer Liste steuern die Tasten wie am Pult das Haupt-Playback.
