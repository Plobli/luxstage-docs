# Einstellungen für Self-Hosting

Diese Tabs erscheinen nur, wenn du LuxStage selbst betreibst (nicht bei einem gehosteten Team unter [luxstage.app](https://luxstage.app)) — dort übernimmt der Betreiber Serverbetrieb, Mailversand, Backups und Updates zentral. Die übrigen Tabs (Konto, Darstellung, Benutzerverwaltung) sind unter [Einstellungen](./einstellungen) beschrieben.

::: tip Update-Benachrichtigung
Ist ein Server-Update verfügbar, zeigt ein kleiner Punkt am Einstellungen-Symbol in der Seitenleiste einen Hinweis darauf.
:::

---

## Anmeldung ohne SMTP

Ist beim Self-Hosting kein Mailversand (SMTP) konfiguriert, entfällt der Link „Passwort vergessen?" auf der Login-Seite. Stattdessen erscheint der Hinweis: „Wende dich an deinen Administrator, um dein Passwort zurücksetzen zu lassen." Ein Admin kann das Passwort unter **Benutzerverwaltung → Passwort zurücksetzen** (siehe [Einstellungen](./einstellungen)) neu vergeben.

---

## Backup

::: tip Sensible Daten im Backup
Das ZIP-Backup enthält die komplette Datenbank inklusive Passwort-Hashes aller Benutzer — entsprechend sorgfältig aufbewahren.
:::

**Backup erstellen**

Lädt alle Show-Daten als ZIP-Archiv herunter. Der Dateiname enthält nur das Datum (z. B. `luxstage-backup-2026-07-25.zip`), keine Uhrzeit — zwei Backups am selben Tag heißen identisch und überschreiben sich im Download-Ordner.

- Klick auf **„ZIP-Backup herunterladen"**
- Der Download startet automatisch

---

**Backup wiederherstellen**

Stellt alle Show-Daten aus einem zuvor erstellten ZIP-Backup wieder her. Fotos werden dabei **ergänzt, nicht ersetzt** — vorhandene Fotos ohne Entsprechung im Backup bleiben erhalten. Der Server beendet sich nach der Wiederherstellung selbst und startet nur automatisch neu, wenn ein Prozessmanager (z. B. PM2, Standard bei Self-Hosting) ihn überwacht.

1. Klick auf **„ZIP-Datei auswählen …"**
2. ZIP-Backup-Datei aus dem Dateisystem wählen
3. Klick auf **„Wiederherstellen"**
4. Bestätigungsdialog bestätigen

::: warning Achtung
Die Datenbank (Shows, Kreise, Abschnitte) wird vollständig durch den Backup-Stand ersetzt. Fotos werden nur ergänzt — Fotos, die im Backup fehlen, bleiben zusätzlich bestehen.
:::

Vor dem Einspielen wird das Backup geprüft: enthält das ZIP eine gültige Datenbank, ist sie unbeschädigt. Schlägt die Prüfung fehl, bleibt der aktuelle Stand **unangetastet**. Mögliche Fehlermeldungen:

- „ZIP enthält keine luxstage.db"
- „Datenbank ist beschädigt oder ungültig"
- „Upload zu groß" — maximale Backup-Größe beim Wiederherstellen: **500 MB**. Größere Datenbestände lassen sich nur über die Kommandozeile auf dem Server wiederherstellen.

Nur Fotos mit den Endungen `jpg`, `jpeg`, `png`, `gif`, `webp` werden beim Wiederherstellen zurückgespielt — andere Dateitypen im ZIP werden stillschweigend übersprungen.

---

## Server

| Feld | Beschreibung |
|------|-------------|
| **Server-URL** | API-Server-Adresse (Standard: http://localhost:3000). Wirkt **sofort** beim Verlassen des Feldes, ohne Speichern-Button — eine falsche Eingabe macht die App unbedienbar. |
| **App-Version** | Aktuell installierte App-Version |
| **Server-Version** | Aktuell installierte Server-Version |
| **Festplatte (frei)** | Verfügbarer Speicherplatz auf dem Server — erscheint nur, wenn der Server erreichbar ist. Sonst steht dort ein Verbindungsfehler. |

---

## E-Mail / SMTP

SMTP-Konfiguration für automatische E-Mails (Willkommen, Passwort-Reset):

| Feld | Beschreibung | Standard |
|------|-------------|---------|
| **SMTP-Host** | Hostname des Mailservers | mail.example.com |
| **Port** | SMTP-Port | 587 |
| **TLS (Port 465)** | Checkbox für TLS-Verschlüsselung | – |
| **Benutzername** | SMTP-Anmeldename | – |
| **Passwort** | SMTP-Passwort | – |
| **Absender (From)** | Absenderadresse | LuxStage <noreply@example.com> |

::: tip Gespeichertes Passwort
Ein bereits gespeichertes SMTP-Passwort wird aus Sicherheitsgründen nie angezeigt — das Feld bleibt leer, nur ein Platzhalter (••••••••) zeigt, dass eines hinterlegt ist. Speicherst du ohne das Feld auszufüllen, bleibt das alte Passwort erhalten.
:::

**Buttons:**
- **„Speichern"** – Einstellungen speichern
- **„Test-Mail senden"** – Öffnet einen Dialog zur Eingabe der Empfängeradresse (vorbelegt mit deiner eigenen E-Mail), sendet danach eine Test-Mail zur Überprüfung der Konfiguration

---

## Update

Prüft auf neue Versionen und aktualisiert den Server. Bei Fehler wird der alte Zustand automatisch wiederhergestellt.

1. **Release** auswählen — die Liste kommt von den GitHub-Releases des Projekts, vorausgewählt ist immer der neueste Eintrag. Die Prüfung auf Updates startet automatisch beim Öffnen des Tabs bzw. bei Release-Wechsel.
2. Ist ein Update verfügbar, zeigt die Seite den Release-Namen und die zugehörigen Release-Notes als Änderungsprotokoll. Ohne verfügbares Update ist der Button **„Jetzt aktualisieren"** gesperrt.
3. Klick auf **„Jetzt aktualisieren"** startet die Aktualisierung. Ein Fortschrittsbalken und ein mitlaufendes Terminal-Protokoll zeigen den Ablauf live.
