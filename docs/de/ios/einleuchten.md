# Einleuchten (iOS)

Der **Einleuchten**-Tab ist die zentrale Fokussier-Ansicht der Show. Er zeigt alle Kreise der Produktion in einer Liste, gruppiert nach **Bühnenpositionen** (z. B. „FOH SL Slot").

## Kreisanzeige

<img src="/img/ios/einleuchten-kanalliste.png" alt="Kreisliste" class="ios-screenshot">

Jeder Kreis wird als Karte mit folgenden Elementen dargestellt:

| Element | Bedeutung |
|---------|-----------|
| **Große Kreisnummer** (z. B. `001`) | Wird rot, sobald der Kreis als fokussiert markiert ist |
| **Name und Gerät** | z. B. „Person Stage Left · 1/1 · ETC Source Four 26°" |
| **Fokus-Kreis** (links) | Tippen → Kreis als fokussiert markieren (roter Haken) |
| **OSC-Toggle** (rechts) | Kreis über OSC auf Full schalten; aktiv = grüner Toggle, Karte rosa hinterlegt |

## Fortschritt

Oben rechts zeigt der Status, wie viele Kreise bereits fokussiert wurden, z. B. `64 · 50%`.

## Suche

Das Suchfeld oben filtert die Kreisliste in Echtzeit nach Name, Gerät oder Notiz.

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
