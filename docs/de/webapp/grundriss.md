# Zeichnung

Der Tab **Zeichnung** bietet einen interaktiven Vektor-Editor für den Bühnengrundplan. Hier können Leuchtenpositionen eingezeichnet, beschriftet und exportiert werden.

## Benutzeroberfläche

### Werkzeugleiste

Alle Werkzeuge tragen eine Beschriftung neben dem Symbol und sind in Gruppen sortiert (Navigation, Zeichnen, Lichttechnik, Maßstab, Hintergrund, Export).

| Symbol | Werkzeug | Tastaturkürzel |
|--------|----------|----------------|
| ▶ Pfeil | **Auswählen** | V |
| ✋ Hand | **Verschieben** (Panning) | H |
| \ Linie | **Linie** zeichnen | L |
| □ Rechteck | **Rechteck** zeichnen | R |
| ○ Ellipse | **Ellipse/Kreis** zeichnen | E |
| T Text | **Text** hinzufügen | T |
| ⊙ Kreis | **Kreis platzieren** | C |
| ↑ Upload | **Hintergrundbild hochladen** | – |
| ⊠ Entfernen | **Hintergrundbild entfernen** | – |
| ↓ Export | **Als PNG exportieren** | – |

### Untere Werkzeuge

| Symbol | Funktion | Tastaturkürzel |
|--------|----------|----------------|
| ↩ | **Rückgängig** | Ctrl+Z |
| ↪ | **Wiederholen** | Ctrl+Y / Ctrl+Shift+Z |
| 🗑 | **Auswahl löschen** | Delete / Backspace |

Weitere Tastaturkürzel des Zeichnungs-Editors siehe [Tastaturkürzel](./tastaturkuerzel).

### Optionsleiste (oben links)

| Option | Funktion | Tastaturkürzel |
|--------|----------|----------------|
| **Gitter** | Gitternetz ein-/ausblenden | G |
| **Einrasten** | Am Gitter einrasten aktivieren/deaktivieren | – |

## Kreise in der Zeichnung platzieren

1. Werkzeug **„Kreis platzieren" (C)** auswählen
2. Auf die gewünschte Stelle in der Zeichnung klicken
3. Die Kreismarkierung erscheint als schlanke, nummerierte Marke. Vor dem Klick zeigt die Vorschau am Mauszeiger bereits die echte Größe.

## Elemente drehen

Zugstangen, Rechtecke, Ellipsen und Texte lassen sich frei drehen: Element anwählen und den gelben Griff über dem Element ziehen. Alternativ drehen die Schaltflächen in der Optionsleiste um 45° oder 90° nach links bzw. rechts. Kreismarken haben keine Ausrichtung mehr.

## Gassengestell

Gassengestelle erscheinen kompakt mit gut lesbarer Beschriftung auf einem deckenden Hintergrund.

## Maßstab-Werkzeug

Der Maßstab muss direkt nach dem Hochladen eines Grundrisses festgelegt werden: Ein Hinweis erklärt das Vorgehen und bietet **Strecke markieren** oder **Später** an. Beim Markieren folgt dem Mauszeiger eine Linie. Zugstangen und Gassengestelle haben in der Vorschau beim Platzieren dieselbe Größe wie danach.

Mit dem Maßstab-Werkzeug (Lineal-Symbol, Tastaturkürzel **Y**) wird die Längenskala der Zeichnung kalibriert. Dadurch werden Zugstangen mit ihrer echten Länge dargestellt.

So funktioniert es:

1. Werkzeug **„Maßstab"** auswählen
2. Zwei Punkte in der Zeichnung anklicken (z. B. zwei Markierungen auf einem Scan), deren reale Entfernung bekannt ist — ein Kreis markiert den ersten Punkt (gelb), eine Linie verbindet die beiden Punkte
3. Ein Dialog öffnet sich und fragt nach der realen Distanz in Metern
4. Die Distanz eingeben (z. B. `6` für 6 Meter) und bestätigen
5. Der Plan ist kalibriert — alle Zugstangen werden danach mit ihrer echten Länge angezeigt

::: info Maßstab-Anzeige
Unten links in der Zeichnung zeigt ein Skalierungs-Balken (white bar) die aktuelle Längenskala an — z. B. „1m" bei einer 1-Meter-Referenzstrecke. Der Balken aktualisiert sich bei Zoom-Änderungen.
:::

---

## Hintergrundbild verwenden

Ein Hintergrundbild (z. B. ein Scan des Bühnenplans) kann auf zwei Wegen hinzugefügt werden:

- **Über die Spielort-Vorlage:** Wird in der Spielort-Vorlage hinterlegt und automatisch in alle Shows übernommen
- **Manuell:** Klick auf das **↑ Upload**-Symbol in der Werkzeugleiste → Bilddatei auswählen

Erlaubte Formate: **PNG, JPG**. Ein PDF-Bühnenplan wird nicht unterstützt und muss vorher umgewandelt werden — bei falschem Format erscheint eine Fehlermeldung.

::: warning Nur ein Hintergrundbild pro Vorlage
Ein neues Hintergrundbild ersetzt das alte sofort und ohne Rückfrage. Anders als Fotos im Fotos-Tab wird das Hintergrundbild **nicht komprimiert oder verkleinert** — ein großer Scan bleibt in voller Größe erhalten und wird bei jedem Öffnen der Zeichnung neu geladen. Für schnelles Laden lohnt es sich, das Bild vorher selbst zu verkleinern.
:::

Zum Entfernen: Klick auf das **⊠**-Symbol.

## Als PNG exportieren

Klick auf das **↓**-Symbol in der Werkzeugleiste → Die aktuelle Zeichnung wird als PNG-Datei heruntergeladen.

::: info Hinweis
Für den Export als PDF (inkl. Kreisliste) nutze **Exportieren → PDF** in der oberen Menüleiste.
:::
