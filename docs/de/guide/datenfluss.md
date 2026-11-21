# Wer trägt wo ein, was erscheint wo

Alle Daten einer Show liegen an einer Stelle: auf deinem LuxStage-Server. Web-App, Desktop-App, iOS- und Android-App sind nur verschiedene Fenster auf dieselbe Show. Was du an einer Stelle einträgst, sehen alle anderen nach dem nächsten Abgleich.

<div class="datenfluss">
<svg viewBox="0 0 720 300" role="img" aria-label="Eingabe in Web-App, Desktop-App, iOS und Android fließt in die Show auf dem Server. Von dort erscheint sie in den Apps, im PDF-Einleuchtplan, im CSV-Export und in der Spielstätten-Vorlage.">
  <g class="df-box">
    <rect x="10" y="30" width="190" height="52" rx="10"/><text x="105" y="61">Web-App · Desktop</text>
    <rect x="10" y="124" width="190" height="52" rx="10"/><text x="105" y="155">iPhone · iPad</text>
    <rect x="10" y="218" width="190" height="52" rx="10"/><text x="105" y="249">Android</text>
  </g>
  <g class="df-core">
    <rect x="265" y="100" width="190" height="100" rx="14"/>
    <text x="360" y="143">Deine Show</text>
    <text x="360" y="167" class="df-sub">auf dem LuxStage-Server</text>
  </g>
  <g class="df-box">
    <rect x="520" y="10" width="190" height="52" rx="10"/><text x="615" y="41">Alle Apps</text>
    <rect x="520" y="86" width="190" height="52" rx="10"/><text x="615" y="117">PDF Einleuchtplan</text>
    <rect x="520" y="162" width="190" height="52" rx="10"/><text x="615" y="193">CSV-Export</text>
    <rect x="520" y="238" width="190" height="52" rx="10"/><text x="615" y="269">Spielstätten-Vorlage</text>
  </g>
  <g class="df-line">
    <path d="M200 56 C235 56 235 130 265 135"/><path d="M200 150 L265 150"/><path d="M200 244 C235 244 235 170 265 165"/>
    <path d="M455 130 C490 120 490 36 520 36"/><path d="M455 142 C490 140 490 112 520 112"/>
    <path d="M455 158 C490 160 490 188 520 188"/><path d="M455 170 C490 180 490 264 520 264"/>
  </g>
</svg>
</div>

<style>
.datenfluss { margin: 24px 0; }
.datenfluss svg { width: 100%; height: auto; }
.datenfluss text { font-size: 15px; text-anchor: middle; fill: var(--vp-c-text-1); font-family: var(--vp-font-family-base); }
.datenfluss .df-sub { font-size: 12px; fill: var(--vp-c-text-2); }
.datenfluss .df-box rect { fill: var(--vp-c-bg-soft); stroke: var(--vp-c-divider); }
.datenfluss .df-core rect { fill: var(--vp-c-brand-soft); stroke: var(--vp-c-brand-1); stroke-width: 2; }
.datenfluss .df-line path { fill: none; stroke: var(--vp-c-brand-1); stroke-width: 2; }
</style>

Fast alles kannst du überall eintragen. Die Tabellen unten nennen die Ausnahmen und zeigen, wo ein Feld später auftaucht.

## Drei Notizen, drei Zwecke

Hier entstehen die meisten Missverständnisse:

| Notiz | Wofür | Wo sichtbar |
|---|---|---|
| **Einleuchtnotiz** (am Kreis) | Was beim Einleuchten zu tun ist, z. B. „auf Sofa, weich“. Das ist der Einleuchthinweis bzw. die Focus-Notiz. | alle Apps, PDF-Einleuchtplan, CSV |
| **Beschriftung** (am Foto) | Was auf dem Bild zu sehen ist | alle Apps, PDF unter dem Foto |
| **Persönliche Anmerkung** (am Kreis) | Deine eigene Gedächtnisstütze | nur für dich, in allen Apps. Nie im PDF oder CSV |

::: tip Faustregel
Soll das ganze Team beim Einleuchten etwas wissen, gehört es in die **Einleuchtnotiz**. Die Fotobeschriftung erklärt nur das Bild.
:::

Eine Einleuchtnotiz kannst du als **Hinweis** markieren (z. B. „Wegdrehen“). Dann ist sie eine Aufgabe statt eines Einleuchtpunkts, siehe [Kreise](/de/webapp/kanaele#notiz-als-hinweis-markieren).

## Kreise

| Feld | Eintragen | Erscheint in |
|---|---|---|
| Kreis, Adresse, Gerät | überall | Apps, PDF, CSV, Vorlage |
| Bühnenposition | überall | Apps, PDF (als Gruppentitel), CSV, Vorlage |
| Gel und 2. Folie | überall | Apps, PDF (auch bei Türmen, Standorten, Obermaschinerie), CSV, Vorlage |
| Einleuchtnotiz | überall | Apps, PDF (nur Kreise mit Notiz), CSV, Vorlage |
| Hinweis-Markierung | überall | Apps, CSV. Nicht im PDF |
| Anzahl | überall | Apps, PDF (ab 2), CSV, Vorlage |
| Prio | überall | Apps, PDF (als Badge), CSV |
| Persönliche Anmerkung | überall | nur für dich |
| Einleuchten-Haken | überall | Apps |
| Kreisgruppen | überall | Apps, Vorlage |
| Montage | entsteht automatisch, wenn du ein Gerät in der Obermaschinerie platzierst | Web-App |

## Fotos

| Feld | Eintragen | Erscheint in |
|---|---|---|
| Foto, Reihenfolge | überall | Apps, PDF |
| Beschriftung | überall | Apps, PDF (einzeilig, gekürzt) |
| Zuordnung zu Kreisen | überall | Apps, PDF („Kreise: 12, 14“ unter dem Foto) |

## Aufbaunotizen, Obermaschinerie, Gassentürme, Standorte

Alle Felder dieser Bereiche trägst du überall ein. Sie erscheinen in allen Apps und im PDF-Einleuchtplan.

- **Obermaschinerie:** Name, Zugnummer, Länge, Höhe, Typ, Notiz je Zug; je Gerät Kreis, Position und Notiz. Ein Gerät mit Kreis übernimmt Gerät und Gel vom Kreis.
- **Gassentürme:** Name, Anzahl Plätze, Notiz je Turm und je Platz.
- **Standorte:** Name, Art, Ort, Hinweis und zugeordnete Kreise. Ein Kreis gehört zu höchstens einem Standort.
- **Aufbaunotizen:** Überschriften, Text und Tabellenzeilen.

## Show-Daten

| Feld | Eintragen | Erscheint in |
|---|---|---|
| Name, Datum | überall | Apps, PDF |
| Spielzeit | überall | Apps, PDF-Kopf |
| Spielstätte | Web-App: nur beim Anlegen. Apps: jederzeit | Apps, PDF |
| Bereiche (Obermaschinerie, Türme, 2. Folie) an/aus | überall | Apps, PDF |
| Archiviert | überall | Apps |

## Nur in der Web-App

- **[Aus EOS importieren](/de/webapp/import-eos)** und **[CSV importieren](/de/webapp/import-csv)**. Beim EOS-Import wählst du, welche Pult-Felder in die Einleuchtnotiz gehen. Alle übrigen Pult-Felder siehst du nur in der Web-App beim Überfahren des Geräts.
- **[Spielstätten-Vorlage](/de/webapp/spielstaette-vorlage)** bearbeiten. Die Apps nutzen die Vorlage beim Anlegen einer Show.

## Was die Spielstätten-Vorlage übernimmt

Eine Vorlage überträgt die feste Ausstattung einer Spielstätte in jede neue Show:

- Kreise mit Adresse, Gerät, Bühnenposition, Gel, 2. Folie, Einleuchtnotiz und Anzahl
- Kreisgruppen und Standorte
- Obermaschinerie mit Geräten und Gassentürme
- Aufbaunotizen: Überschriften und Tabellenzeilen, Texte starten leer

Nicht in der Vorlage: Prio, Hinweis-Markierung, Spielzeit und alles Persönliche. Das gehört zur einzelnen Show.

Das PDF der Vorlage ist ein Vordruck: Kreis, Adresse und Gerät sind gedruckt, der Rest bleibt zum Ausfüllen frei.
