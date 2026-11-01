# Kreisliste scannen

Neben dem [EOS-Import](./import-eos) und dem [CSV-Import](./import-csv) gibt es einen dritten Weg, eine Kreisliste zu befüllen: ein Foto einer ausgefüllten Kreisliste hochladen und per KI automatisch auslesen lassen.

::: tip Vordruck herunterladen
Für den Scan eignet sich am besten der Kreislisten-Vordruck. Diesen vorher unter **Vorlagen** herunterladen und ausdrucken, ausfüllen (z. B. per Hand am Aufbautag) und danach fotografieren. Eine komplett handschriftliche Liste ohne Vordruck funktioniert ebenfalls.
:::

## Foto hochladen

1. In LuxStage auf **„Importieren"** klicken → **„Kreisliste scannen"** auswählen
2. Foto der ausgefüllten Kreisliste aus dem Dateisystem auswählen
3. Die KI liest das Bild aus — während der Auswertung erscheint der Hinweis „Kreisliste wird ausgewertet …"

## Was wird ausgelesen?

Die KI erkennt pro Zeile so viele der folgenden Angaben wie im Foto lesbar sind:

- **Kreisnummer** (Pflichtangabe, ohne die eine Zeile nicht übernommen werden kann)
- **Adresse** (DMX-Adresse)
- **Gerät**
- **Bühnenposition** — auch wenn diese nur einmal als Gruppenüberschrift über mehreren Zeilen steht, statt in jeder Zeile einzeln
- **Filter/Farbe**
- **Notizen**

Bereits in der Show vorhandene Kreise dienen der KI dabei als Lesehilfe (z. B. um unklare Handschrift plausibler zuzuordnen) — sie werden dadurch nicht automatisch verändert, das geschieht erst über die Vorschau.

::: warning Foto-Qualität
Handschrift kann unsauber ausgelesen werden. Bei Unklarheiten wählt die KI die plausibelste Lesart. Ergebnisse vor dem Übernehmen in der Vorschau prüfen.
:::

## Vorschau und Auswahl

Nach der Auswertung öffnet sich der Dialog **„Kreisliste-Scan — Vorschau"** mit bis zu zwei Gruppen (jeweils mit Zähler in Klammern):

- **Aktualisierte Kreise (n)** — bereits vorhandene Kreise, bei denen sich laut Scan etwas geändert hat
- **Neue Kreise (n)** — im Scan erkannte Kreise, die in der Show noch nicht existieren

Jede erkannte Änderung lässt sich **einzeln abwählen**, bevor sie übernommen wird. Jede Gruppe hat einen eigenen **„Alle umschalten"**-Link oben rechts, um die Auswahl innerhalb dieser Gruppe zu kehren.

Wurden im Foto keine ausgefüllten Zeilen erkannt, erscheint der Hinweis „Keine ausgefüllten Zeilen erkannt."

Sollte die KI-Auswertung länger als 45 Sekunden dauern, bricht der Scan ab und zeigt eine Fehlermeldung.

## Übernehmen

Klick auf **„Übernehmen (n)"** wendet nur die ausgewählten Änderungen an (n = Anzahl ausgewählter Kreise). Eine Bestätigung zeigt, wie viele Kreise aktualisiert und wie viele neu angelegt wurden.

::: warning Foto wird an die Anthropic-API übertragen
Der Scan nutzt ein KI-Modell von Anthropic (Claude Vision). Das hochgeladene Foto wird dafür an die Anthropic-API übertragen — anders als bei den übrigen Funktionen der Web-App, die ausschließlich mit dem eigenen LuxStage-Server kommunizieren. Details dazu in der [Datenschutzerklärung](https://luxstage.app/datenschutz.html).
:::
