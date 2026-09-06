# ToDo — Review Kunden-Dokumentation Web-App

**Anweisung:** 
- Nach jedem Punkt einen commit machen ohne Versionserhöhung
- so wenig wie möglich Zwischentexte während der Bearbeitung ausgeben. 
- Fertige Punkte abhaken

Stand: 2026-07-25. Vergleich `LuxStage-Docs/docs/{de,en}/` gegen `LuxStage/web-app/src` + `LuxStage/server`.

## A. Fehlende Seiten (komplett undokumentiert)

- [x] **Registrierung & Login** — ✅ teilweise erledigt (2026-07-26): Neue Seite `login.md` (DE+EN) für Anmeldung und Passwort-vergessen-Flow (SMTP-abhängig), in Sidebar eingetragen. **Registrierung (Team anlegen) bewusst ausgelassen** — auf Wunsch, da SaaS-spezifisch (erzeugt `<team>.luxstage.app`, nicht relevant für Self-Hoster).
- [x] **Show-Health-Badge / Vollständigkeitsprüfung** — ✅ erledigt (2026-07-26): Abschnitt in `kanaele.md` (DE+EN) ergänzt. Hinweis: „keine Notiz" wird laut Code aktuell **nicht** in die Zählung/Filter einbezogen (nur Gerät/Position/Adresse), Doku entsprechend auf drei Filter beschränkt.
- [x] **Presence / Live-Zusammenarbeit in der Web-App** — ✅ erledigt (2026-07-26): Abschnitt in `kanaele.md` (DE+EN) ergänzt.
- [x] **Automatisch generierter Text** — ✅ erledigt (2026-07-26): Abschnitt in `info.md` (DE+EN) ergänzt.
- [x] **Update-Benachrichtigung** — ✅ erledigt (2026-07-26): Tipp-Box in `einstellungen.md` (DE+EN) ergänzt.
- [x] **Gehostete Variante (SaaS) / Betreiber-Panel** — bewusst nicht dokumentiert (Entscheidung Christopher, 2026-07-26): intern, nicht für die öffentliche Kunden-Doku bestimmt.
- [x] **Docker-Installation** — ✅ erledigt (2026-07-26): vollständiger Abschnitt in `installation.md` (DE+EN) mit Schritten, `.env`-Beispiel und Hinweis auf fehlendes automatisches HTTPS.

## B. Inhaltliche Fehler / Widersprüche

- [x] **Terminologie uneinheitlich: Vorlage / Template / Spielort / Spielstätte / Bühne.** — ✅ erledigt (2026-07-26)
  Web-App und iOS sagen jetzt durchgehend **„Spielort-Vorlage"** (englisch „venue template") — siehe 2.2 in [TODO-webapp-code.md](./TODO-webapp-code.md). Doku nachgezogen:
  - Sidebar-Eintrag in `webapp/index.md` auf „Spielort-Vorlage" geändert
  - Dateiname `spielstaette-vorlage.md` **nicht** umbenannt (Aufwand/Nutzen), aber Inhalt komplett auf „Spielort-Vorlage" umgestellt
  - Alle „Bühnen-Template"-Stellen ersetzt: `spielstaette-vorlage.md` (20+ Stellen), `de/ios/einstellungen.md`, `de/ios/osc.md`, `de/webapp/grundriss.md:58`, `de/webapp/info.md:3`
  - „Kanaltemplate" → „Kanalstruktur" in `de/webapp/index.md`, `de/webapp/shows.md`, `de/ios/shows.md`
  - `features.md`: „Spielstätten-Vorlagen" → „Spielort-Vorlagen"
  - EN-Pendants aller genannten Dateien mitgezogen → „venue template" / „venue"
  - Web-App-Route bleibt `/templates`, View `TemplatesView.vue` (interne Bezeichner unverändert)
- [ ] **`webapp/index.md`: „Die Seitenleiste enthält vier Symbole"** — Router hat Shows, Archiv, Vorlagen, Einstellungen = 4. Prüfen, ob Zählung und Reihenfolge noch stimmen, wenn Registrierung/Login ergänzt wird.
- [ ] **`installation.md`: Zugangsdaten `admin` / `tech` als „Benutzername"** — Web-App und `users.js` arbeiten mit E-Mail-Adressen. Klären, ob der Installer wirklich reine Benutzernamen anlegt, und ggf. korrigieren.
- [ ] **`einstellungen.md`: Rollen** — nennt nur `admin` und `techniker`. Prüfen, ob durch das Operator-Panel eine dritte Rolle existiert und ob „Techniker" wirklich keine Vorlagen bearbeiten darf (Aussage steht in `features.md` und `installation.md` leicht abweichend).
- [x] **`setup.md` Tipp-Box** — ✅ bereits korrekt: verweist auf Info-Tab, unverändert übernommen.
- [x] **`features.md`: „Alle 10 Minuten wird ein Snapshot gespeichert"** — ✅ erledigt (2026-07-26): Intervall stimmt (`INTERVAL_MS`, `history.js:20`), bestätigt.
- [x] **`features.md`, Abschnitt Aufbaunotizen** — ✅ erledigt (2026-07-26): doppelter Punkt entfernt.
- [x] **`features.md`: „Rich-Text-Editor mit Markdown … Links und Bilder"** — ✅ erledigt (2026-07-26): gegen `MarkdownEditor.vue` verifiziert, Text auf tatsächliche Buttons korrigiert (Fett, Kursiv, Überschrift, Aufzählung, nummerierte Liste, Tabelle — kein H1–H4, keine Links/Bilder).
- [x] **`info.md`: Werkzeugleiste** — ✅ erledigt (2026-07-26): `features.md` an `info.md` angeglichen (beide „Überschrift" ohne Ebenen).

## C. Zu dünne Seiten

- [x] **`import-csv.md`** — ✅ erledigt (2026-07-26): Spaltenschema, Trennzeichen, Encoding, Merge-Verhalten ergänzt (DE+EN). Fehlermeldungen (`csv.error.*`) nicht ergänzt — Keys sind im Code tot (kein Aufrufer gefunden), der Parser wirft aktuell keine Fehler.
- [x] **`export-pdf.md`** — ✅ erledigt (2026-07-26): Grundriss ergänzt, Foto-Einschränkungen ergänzt (siehe Abschnitt Q). Button-Ort und Vorschau-Dialog nicht ergänzt — Export läuft direkt ohne Vorschau-Dialog.
- [x] **`export-csv.md`** — ✅ erledigt (2026-07-26): Spalten, Trennzeichen, Dateiname ergänzt (DE+EN).
- [x] **`import-eos.md`** — ✅ erledigt (2026-07-26): Merge-Dialog-Gruppen und Notizen-Erhalt dokumentiert (siehe Abschnitt S).
- [x] **`fotos.md`** — ✅ erledigt (2026-07-26): Drag & Drop-Upload, Lightbox/Vollbild-Navigation und Foto löschen ergänzt (DE+EN). „Sortieren per Drag & Drop" existiert in `PhotoGallery.vue` **nicht** — Befund war falsch, nicht ergänzt.
- [x] **`archiv.md`** — ✅ erledigt (2026-07-26): geprüft, keine Sortierung/Suche vorhanden — in `archiv.md` (DE+EN) korrigiert (siehe Abschnitt T).

## D. Fehlende Screenshots

- [ ] Web-App hat nur **zwei** Bilder (`img/webapp/import-eos/`), die iOS-Doku dagegen ~24. Screenshots ergänzen für: Shows-Übersicht, Kanaltabelle, Setup (Gestelle + Zugstangen), Info-Tab, Fotos-Galerie, Grundriss-Editor, Versionsverlauf-Panel, Einstellungen-Tabs.
- [ ] `webapp/index.md` beschreibt die Seitenleiste rein textlich — ein Screenshot würde das ersetzen.

## E. Zweisprachigkeit (EN)

- [x] Alle DE-Seiten haben ein EN-Pendant — ✅ weiterhin gepflegt, bei jeder Änderung in diesem Review beide Sprachen mitgezogen.
- [x] **EN-Dateinamen sind deutsch** — ✅ erledigt (2026-07-26): `en/webapp/kanaele.md`→`channels.md`, `spielstaette-vorlage.md`→`venue-template.md`, `en/ios/aufbau.md`→`setup.md`, `einleuchten.md`→`focus.md`. Alle internen Links und `config.js` angepasst.
- [x] **`en/webapp/versionsverlauf.md`** → `version-history.md`, `fotos.md` → `photos.md`, `archiv.md` → `archive.md`, `einstellungen.md` → `settings.md`, `grundriss.md` → `floor-plan.md` — ✅ erledigt (2026-07-26). Zusätzlich mitgezogen: `en/glossar.md` → `glossary.md`, `en/webapp/tastaturkuerzel.md` → `keyboard-shortcuts.md`, `en/ios/einstellungen.md` → `settings.md`.

## F. Struktur & Navigation

- [x] **`features.md` überschneidet sich stark mit den Anleitungsseiten** — ✅ erledigt (2026-07-26): Datei von `webapp/features.md` nach `/features.md` verschoben (Top-Level, deckt beide Apps ab), in Guide-, Web-App- und iOS-Sidebar verlinkt (DE+EN).
- [x] **Sidebar-Gruppe „Shows"** enthält auch „Einstellungen" — ✅ erledigt (2026-07-26): neue Gruppe „Verwaltung"/„Management" mit Archiv, Spielort-Vorlage, Einstellungen (DE+EN).
- [x] **Kein Glossar** — ✅ erledigt (2026-07-26): neue Seite `glossar.md` (DE+EN) mit allen genannten Begriffen, in Guide-, Web-App- und iOS-Sidebar verlinkt.
- [x] **`docs/android-plan.md`** — ✅ erledigt (2026-07-26): nach `LuxStage-Docs/android-plan.md` verschoben, außerhalb des VitePress-Build-Ordners.
- [x] **Keine Seite zu Tastaturkürzeln gesamt** — ✅ erledigt (2026-07-26): neue Seite `tastaturkuerzel.md` (DE+EN), in Sidebar unter „Referenz" eingetragen.

## G. Prüfaufgaben (vor Umsetzung verifizieren)

- [ ] Snapshot-Intervall in `server/history.js` gegen „alle 10 Minuten" abgleichen.
- [ ] Rollenrechte in `server/auth.js` / `routes/users.js` gegen die Rollentabellen in `einstellungen.md`, `features.md` und `installation.md` abgleichen — drei Stellen, drei Formulierungen.
- [ ] Grundriss-Tastaturkürzel in `composables/floorplan/useFloorplanState.ts` gegen die Tabelle in `grundriss.md` prüfen.
- [ ] Maßeinheiten: `routes/display.js` erlaubt `m`, `cm`, `mm` — passt zu `einstellungen.md`. OK.
- [ ] „Fotos pro Druckseite: 1, 2, 4, 6, 8, 9, 12" gegen `usePhotoSettings.ts` prüfen.
- [ ] Offline-Aussage in `faq.md` („Web-App zeigt gespeicherte Daten ohne Serververbindung") gegen `api/cache.ts` verifizieren — kritische Kundenzusage.

---

# Runde 2 — Nutzersicht

Methodik: `shared/locales/de.json` (434 Keys) ist die vollständige Liste **aller Texte, die ein Nutzer je zu sehen bekommt**. Jeder Key wurde gegen die Doku geprüft. Ergänzt um Prüfung, ob jemand ohne Vorkenntnisse die Doku durcharbeiten kann.

## H. Begriffe: Doku sagt X, die App zeigt Y

Der Nutzer sucht nach dem Wort, das auf seinem Bildschirm steht. Findet er es in der Doku nicht, ist die Seite für ihn wertlos.

- [x] **„Position" vs. „Kategorie"** — ✅ erledigt (2026-07-25): App auf „Position" vereinheitlicht, „Kategorie" kommt in Web-App, iOS und Website nicht mehr vor. `kanaele.md` stimmt damit bereits; die Doku muss nur noch prüfen, ob irgendwo „Kategorie" als Suchwort steht. Details siehe 2.1 in `TODO-webapp-code.md`.
- [x] **„Vorlage" vs. „Template"** — ✅ überholt (2026-07-26): `nav.templates` zeigt jetzt „Vorlagen" (Code-Todo 2.2), Doku sagt ebenfalls „Vorlagen". Kein Widerspruch mehr.
- [x] **„Spielort" vs. „Bühne" vs. „Spielstätte"** — ✅ überholt (2026-07-26): `show.assign_template`, `field.venue`, `template.venue_name` existieren nicht mehr (waren tote Keys, in Code-Todo 2.2 entfernt). Nur noch „Spielort-Vorlage" durchgehend.
- [x] **Tab „Setup"** — ✅ erledigt (2026-07-26): `setup.md`/EN ergänzt, dass der Zugstangen-Abschnitt als Unter-Tab „Obermaschinerie" (`tab.obermaschinerie`) in der App erscheint. `tab.buehne` existiert in `de.json` nicht mehr (veraltet, ignoriert). Neuer Fund: **`tab.gassenturm` ist in der App selbst uneinheitlich übersetzt** — DE „Setup", EN „Stage Plan" (`en.json:349`), für denselben Tab. Gehört in die Code-ToDo, nicht in die Doku behoben.
- [x] **`tab.raum` = „Raum", `tab.hinweise` = „Hinweise"** — ✅ überholt (2026-07-26): Beide Keys existieren in `de.json` nicht mehr (Code-Todo 2.3 hat sie entfernt, Icon-Zuordnung läuft jetzt über `icon`-Spalte statt Titelvergleich). Keine Doku-Änderung nötig.

## I. Undokumentierte Funktionen (Runde 2)

- [x] **„Auf alle Shows anwenden"** — ✅ erledigt (2026-07-26): Abschnitt in `spielstaette-vorlage.md` (DE+EN) ergänzt, inkl. Hinweis auf ungefährliche Operation (nur fehlende Elemente).
- [ ] **Offline-Banner** (`offline.banner` = „Keine Verbindung zum Server – Änderungen werden nicht gespeichert") — das **widerspricht direkt** der FAQ-Aussage „Funktioniert LuxStage auch offline? Ja. … Änderungen werden synchronisiert, sobald die Verbindung wiederhergestellt ist." Die Web-App speichert offline **nicht**. FAQ korrigieren — sonst Datenverlust beim Nutzer, der sich auf die Zusage verlässt.
- [x] **Inline-Hilfe (⌘-Icons) in der App** — ✅ erledigt (2026-07-26): Hinweis in `kanaele.md` (DE+EN) ergänzt.
- [x] **Doppelte-Adresse-Warnung** — ✅ erledigt (2026-07-26): Tipp-Box in `kanaele.md` (DE+EN) ergänzt.
- [x] **Show-Metadaten nachträglich ändern** — ✅ erledigt (2026-07-26): Abschnitt in `shows.md` (DE+EN) ergänzt.
- [x] **„Abschnitt hinzufügen" direkt in der Show** — ✅ erledigt (2026-07-26): neuer Abschnitt „Eigenen Abschnitt anlegen" in `info.md` (DE+EN).
- [x] **Feld-Einheit** — ✅ erledigt (2026-07-26): dritte Spalte „Einheit" in `info.md` (DE+EN) ergänzt.
- [x] **Foto löschen** — ✅ erledigt (2026-07-26): Abschnitt „Foto löschen" in `fotos.md` (DE+EN) ergänzt (siehe Abschnitt U).
- [x] **Kanal-Farbwahl „No Color" / Freitext** — ✅ erledigt (2026-07-26): in `kanaele.md` (DE+EN) ergänzt.
- [x] **404-Seite** — bewusst nicht dokumentiert (unkritisch, selbsterklärend).

## J. Widersprüche zwischen Doku und App-Texten

- [x] **Farb-Legende der Kanalnummer.** — ✅ erledigt (2026-07-26): in `kanaele.md` (DE+EN) auf App-Text korrigiert (Weiß/Grün/Gelb).
- [x] **Passwort-Mindestlänge.** — ✅ überholt (2026-07-26): Code-Todo 1.1 hat eine einzige Quelle (`PASSWORD_MIN_LENGTH = 8`) eingeführt, alle Texte leiten sich davon ab. `installation.md` stimmt bereits, kein Widerspruch mehr.
- [x] **Passwort vergessen.** — ✅ Grundlage überholt (2026-07-26): Code-Todo 1.2 hat den Link jetzt an die SMTP-Konfiguration gekoppelt — ist SMTP eingerichtet, erscheint der E-Mail-Flow, sonst der Admin-Hinweis. Dokumentation dieses Flows gehört zu Punkt **A** (Registrierung & Login fehlt komplett) — dort zu erledigen, keine Dopplung hier.
- [x] **Login-Feld heißt „E-Mail-Adresse"** — ✅ überholt (2026-07-26): Code-Todo 1.3 + 7.5 haben das behoben — Installer legt den Admin jetzt mit E-Mail an (`bootstrap.js`), Login-Fehlermeldung sagt „E-Mail-Adresse". Kein Widerspruch mehr, `installation.md` bereits konsistent.
- [x] **Beleuchtungsgestelle aus Vorlage.** — ✅ erledigt (2026-07-26): `setup.md` (DE+EN) auf „Einfügen im Bearbeiten-Dialog" korrigiert.
- [x] **`info.md` beschreibt Abschnitte als vorgegeben** — ✅ erledigt (2026-07-26): siehe I, Abschnitt „Eigenen Abschnitt anlegen" ergänzt.
- [x] **`einstellungen.md`: „Passwort zurücksetzen"** — ✅ bereits korrekt: steht in der Doku nur unter „Benutzerverwaltung" (Admin-Bereich), nicht unter „Konto". Kein Fix nötig, Befund war veraltet.

## K. Datenschutzerklärung — sachlich falsch

- [x] **`datenschutz.md` gilt nur für die iOS-App** — ✅ erledigt (2026-07-26): Web-App/Self-Hosting-Abschnitt ergänzt, Verantwortlichkeit (Self-Hoster vs. Betreiber luxstage.app) geklärt.
- [x] **Aussage „keine Kommunikation mit Drittanbietern" unzutreffend (OCR/Anthropic)** — ✅ überholt (2026-07-26): geprüft und bestätigt (auf Hinweis von Christopher) — **das OCR-Feature existiert nicht mehr**. Kein Swift-Code ruft es auf, keine Server-Route nutzt `anthropicApiKey` mehr. Nur zwei verwaiste Locale-Keys (`ocr.intro.*`) und die ungenutzte Config-Variable sind übrig. Aussage in der Datenschutzerklärung ist damit korrekt, keine Änderung nötig.
- [x] **App-Store-Datenschutzlabel prüfen** — ✅ überholt: gegenstandslos, da kein Datenfluss an Anthropic mehr existiert.
- [x] **OCR-Feature selbst ist undokumentiert** — ✅ überholt: Feature existiert nicht mehr, keine Doku nötig.
- [x] **Kein Impressum** — ✅ teilweise erledigt (2026-07-26): Warnbox in `datenschutz.md` ergänzt, die auf das fehlende Impressum für luxstage.app hinweist. Kein Impressum auf `LuxStage-Website/` gefunden — bleibt offener Punkt für Christopher, nicht selbst erfunden.

## L. Verständlichkeit für Erstnutzer

- [x] **Kein durchgehender „Von null zur ersten Show"-Pfad.** — ✅ erledigt (2026-07-26): `guide/index.md` (DE+EN) zu „Schnellstart in 10 Minuten" mit direkten Links zu jedem Schritt umgebaut.
- [x] **Fachbegriffe ungeklärt** — ✅ erledigt (2026-07-26): alle genannten Begriffe im neuen `glossar.md` erklärt (siehe Abschnitt F).
- [x] **`kanaele.md`: „KANAL | Kanalname im Pult (links) / Dimmer-Adresse (rechts nach dem ‚/')"** — ✅ erledigt (2026-07-26): Beispiel „1/001" ergänzt (DE+EN).
- [x] **`setup.md` ist mit 110 Zeilen die längste Anleitungsseite** — ✅ erledigt (2026-07-26): aufgeteilt in `setup-gestelle.md` und `setup-zugstangen.md` (DE+EN), alle internen Links und die Sidebar angepasst.
- [x] **Keine Seite „Was tun bei Problemen?"** — ✅ erledigt (2026-07-26): neue Seite `troubleshooting.md` (DE+EN), in Sidebar unter „Referenz" eingetragen. `csv.error.*` nicht aufgenommen — Keys sind tot (siehe unten).
- [x] **CSV-Fehlermeldungen dokumentieren** — ✅ überholt (2026-07-26): `csv.error.*`-Keys sind im Code tot (kein Aufrufer in `web-app/src`), der CSV-Parser wirft aktuell keine Fehler. Das Spaltenschema selbst ist bereits in `import-csv.md` dokumentiert (Abschnitt C).
- [x] **EOS-Import-Dialoge** — ✅ überholt (2026-07-26): Beide Keys existieren nicht mehr, ersetzt durch `EosMergePreviewDialog.vue` — bereits in `import-eos.md` dokumentiert (siehe Abschnitt S).

## M. Zweisprachigkeit — App vs. Doku

- [x] **`de.json` und `en.json` sind vollständig synchron** — ✅ bestätigt (2026-07-26): aktuell 616 Keys in beiden Dateien, exakt gleiche Anzahl. `template.apply_to_shows` in EN ergänzt (Code-Todo 11), `show.template.optional` als toter Key entfernt (Code-Todo 2.2). **App-Übersetzung weiterhin in gutem Zustand.**
- [x] **Die englische Doku übersetzt deutsche Fachbegriffe, die in der App englisch anders lauten.** — ✅ erledigt (2026-07-26): `en/webapp/kanaele.md` gegen `en.json` geprüft und korrigiert (Spaltenköpfe „Chan"/„Qty." statt „CHANNEL"/„QTY", „Custom" statt „free text", „Search channels …"). **Randbefund:** `gassenturm.field.name` in `en.json` ist unübersetzt geblieben („Bezeichnung") — Code-Bug, siehe Punkt 12 in `TODO-webapp-code.md`, nicht in der Doku behebbar.

---

# Runde 3 — Detailprüfung (Dateien vollständig gelesen)

Methodik: `install.sh`, `bootstrap.js`, `history.js`, `pdf.js` und der Tastatur-Handler von `FloorplanEditor.vue` vollständig gelesen statt gegreppt. Genau die Tabellen geprüft, die bisher ungeprüft blieben.

## N. `installation.md` — die kritischste Seite, mehrere Fehler

Verifiziert gegen [install.sh](LuxStage/install.sh) und [server/bootstrap.js](LuxStage/server/bootstrap.js).

- [x] **Der Installer fragt das Admin-Passwort ZWEIMAL ab.** — ✅ erledigt (2026-07-26): in `installation.md` (DE+EN) ergänzt, inkl. Hinweis auf drei Fehlversuche.
- [x] **Prompt-Text weicht ab.** — ✅ erledigt (2026-07-26): auf „Systemnutzer für LuxStage [luxstage]:" (DE+EN) korrigiert.
- [x] **Externe Domain: Doku zeigt falsches Format.** — ✅ erledigt (2026-07-26): DE + EN auf `https://luxstage.example.com` (mit Schema) korrigiert.
- [ ] **Zugangsdaten sind tatsächlich Benutzernamen, keine E-Mail-Adressen.** `bootstrap.js` legt via `INSERT INTO users (username, ...)` die Konten `admin` und `tech` an. Damit ist der offene Punkt aus Runde 2 geklärt: Die Doku hat recht, **die App ist falsch beschriftet** (`auth.username` = „E-Mail-Adresse"). Gehört in die Code-ToDo, nicht in die Doku.
- [x] **Voraussetzungen fehlen komplett.** — ✅ erledigt (2026-07-26): Warnbox in `installation.md` (DE+EN) ergänzt (root/sudo, TTY, apt-get, Debian/Ubuntu/RPi OS).
- [x] **Der Installer ändert den System-Hostname** — ✅ erledigt (2026-07-26): in derselben Warnbox erwähnt.
- [x] **Installierte Fremdpakete nicht genannt** — ✅ erledigt (2026-07-26): in `installation.md` (DE+EN) unter Schritt 4 aufgelistet.
- [x] **Doku sagt „Das Script lädt alles herunter"** — ✅ erledigt (2026-07-26): auf „lädt das neueste GitHub-Release, nicht main" korrigiert (DE+EN).
- [x] **Port 3000 ist fest verdrahtet** — Troubleshooting beschreibt die Änderung bereits korrekt, keine Änderung nötig. ✓
- [x] **Doku: „Der Server startet neu und die LuxStage-Services starten automatisch."** — ✅ erledigt (2026-07-26): Reboot als „empfohlen, nicht zwingend" dargestellt (DE+EN).
- [x] **CORS wird automatisch konfiguriert** — ✅ erledigt (2026-07-26): Hinweis in Schritt 4 ergänzt (DE+EN).

## O. `versionsverlauf.md` — Verhalten unvollständig

Verifiziert gegen [server/history.js](LuxStage/server/history.js).

- [x] **Maximal 50 Versionen pro Show** — ✅ erledigt (2026-07-26): in `versionsverlauf.md` (DE+EN) ergänzt.
- [x] **Snapshots nur bei tatsächlicher Änderung.** — ✅ erledigt (2026-07-26): neuer Abschnitt „Wann werden Versionen gespeichert?" in `versionsverlauf.md` (DE+EN).
- [x] **Zusätzlicher Snapshot beim Öffnen einer Show** — ✅ erledigt (2026-07-26): im selben Abschnitt ergänzt.
- [x] **Das 10-Minuten-Intervall stimmt** (`INTERVAL_MS`, `history.js:20`). Offener Prüfpunkt aus Runde 1 erledigt. ✓
- [x] **Archivierte Shows erhalten keine Snapshots** — ✅ erledigt (2026-07-26): im selben Abschnitt ergänzt.
- [x] **Der Verlauf umfasst nur Kanäle und Abschnitte** — ✅ erledigt (2026-07-26): in `versionsverlauf.md` (DE+EN) klargestellt, inkl. Bestätigungsdialog-Text.

## P. `grundriss.md` — Tastaturkürzel-Tabelle fehlerhaft

Verifiziert gegen den Handler in [FloorplanEditor.vue:1439-1470](LuxStage/web-app/src/components/FloorplanEditor.vue#L1439-L1470).

- [x] **„Kanal platzieren (C)" funktioniert nicht wie beschrieben.** — ✅ überholt (2026-07-26): Code-Todo 7.2 hat den Bug behoben (Bedingung entfernt, Großbuchstabe ergänzt). Doku-Text war bereits korrekt, keine Änderung nötig.
- [x] **Leertaste = temporäres Verschieben** — ✅ erledigt (2026-07-26): in `grundriss.md` (DE+EN) ergänzt.
- [x] **Umschalt+Pfeiltaste verschiebt um 10 statt 1 Einheit** — ✅ erledigt (2026-07-26): in `grundriss.md` (DE+EN) ergänzt.
- [x] **Rückschritt (Backspace) löscht ebenfalls** — ✅ erledigt (2026-07-26): in `grundriss.md` (DE+EN) ergänzt.
- [x] **„Einrasten" hat kein Kürzel** — die Doku führt es korrekt mit „–". ✓
- [x] **Ansicht zurücksetzen: F und Strg+0 stimmen** (`:1449`, `:1470`). ✓ Ebenso Kopieren/Einfügen/Duplizieren/Alles auswählen und Rückgängig/Wiederholen. ✓
- [x] **Esc ist mehrstufig** — ✅ erledigt (2026-07-26): in `grundriss.md` (DE+EN) als „Werkzeug abbrechen / Auswahl aufheben" ergänzt.
- [ ] **`composables/floorplan/useFloorplanState.ts` ist eine leere Datei (0 Zeilen)** — für die Doku irrelevant, gehört aber aufgeräumt.

## Q. PDF-Export — Doku verspricht zu viel

Verifiziert gegen [server/pdf.js](LuxStage/server/pdf.js).

- [x] **„Fotos pro Druckseite" wirkt im PDF NICHT.** — ✅ überholt (2026-07-26): Code-Todo 7.1 hat das Verhalten geändert — die Einstellung liegt jetzt serverseitig und wirkt auf **beide** Ausgaben gleich. `fotos.md`, `export-pdf.md`, `einstellungen.md` (DE+EN) entsprechend bestätigt/korrigiert.
- [x] **Der Grundriss ist im PDF enthalten** — ✅ erledigt (2026-07-26): `features.md`-Tabelle (DE+EN) um „Grundriss" ergänzt.
- [x] **Fotos ohne lesbare Datei werden übersprungen** — ✅ erledigt (2026-07-26): Hinweis in `export-pdf.md` (DE+EN) ergänzt.
- [x] **Foto-Beschriftungen werden einzeilig abgeschnitten** — ✅ erledigt (2026-07-26): im selben Hinweis ergänzt.

---

# Runde 4 — Settings-Views, Import-Dialoge, Listen

Methodik: `SmtpView`, `BackupView`, `UpdateView`, `ServerView` vollständig gelesen; `EosMergePreviewDialog`, `ShowsView`, `ArchiveView` geprüft.

## R. `einstellungen.md` — Abweichungen im Detail

- [x] **„Test-Mail senden" fragt nach einer Empfängeradresse.** — ✅ erledigt (2026-07-26): in `einstellungen.md` (DE+EN) ergänzt. Hinweis: Code-Todo 8.5 hat den `prompt()` bereits durch einen echten Dialog ersetzt.
- [x] **SMTP-Passwort wird beim Laden nie angezeigt.** — ✅ erledigt (2026-07-26): Tipp-Box in `einstellungen.md` (DE+EN) ergänzt.
- [x] **Backup herunterladen dürfen ALLE Benutzer, Wiederherstellen nur Admins.** — ✅ überholt (2026-07-26): Code-Todo 8.2 hat Download wieder admin-only gemacht (Sicherheitsgrund: ZIP enthält Passwort-Hashes). Doku entsprechend auf „beide admin-only" korrigiert.
- [x] **Wiederherstellen ist zweistufig.** — ✅ erledigt (2026-07-26): Schritt-für-Schritt-Anleitung in `einstellungen.md` (DE+EN) korrigiert.
- [x] **Update-Button ist gesperrt, solange keine Aktualisierung vorliegt** — ✅ erledigt (2026-07-26): in `einstellungen.md` (DE+EN) ergänzt.
- [x] **Die Branch-Liste kommt vom Server** — ✅ erledigt (2026-07-26): im selben Absatz ergänzt.
- [x] **Live-Protokoll während des Updates** — ✅ erledigt (2026-07-26): im selben Absatz ergänzt.
- [x] **„Prüfe auf Updates" zeigt die Zahl der neuen Änderungen** — ✅ erledigt (2026-07-26): im selben Absatz ergänzt.
- [x] **Server-Tab: die Doku listet vier Felder, es sind drei plus Eingabefeld.** — ✅ erledigt (2026-07-26): „Festplatte (frei)" als bedingt beschrieben.
- [x] **Server-URL wirkt sofort beim Verlassen des Feldes** — ✅ erledigt (2026-07-26): Warnhinweis in der Tabelle ergänzt.

## S. EOS-Import — Merge-Dialog dokumentieren

Verifiziert gegen [EosMergePreviewDialog.vue](LuxStage/web-app/src/components/EosMergePreviewDialog.vue).

- [x] Der Dialog zeigt **drei Gruppen** — ✅ erledigt (2026-07-26): alle drei in `import-eos.md` (DE+EN) benannt.
- [x] Die dritte Gruppe beantwortet die zentrale Nutzerfrage beim Re-Import — ✅ erledigt (2026-07-26): Tipp-Box „Bestehende Notizen bleiben erhalten" ergänzt.
- [x] Bei fehlenden Änderungen erscheint „Keine Änderungen." — ✅ erledigt (2026-07-26): ergänzt.

## T. Shows- und Archiv-Ansicht

- [x] **Standardsortierung ist „Stand" absteigend** — ✅ erledigt (2026-07-26): in `shows.md` (DE+EN) ergänzt.
- [x] **Sortiert wird innerhalb der Spielort-Gruppen** — ✅ erledigt (2026-07-26): in `shows.md` (DE+EN) klargestellt.
- [x] **Spalten blenden sich abhängig von der Fensterbreite aus** — ✅ erledigt (2026-07-26): Tipp-Box in `shows.md` (DE+EN) ergänzt.
- [x] **Das Archiv bietet keine Sortierung.** — ✅ erledigt (2026-07-26): `archiv.md` (DE+EN) korrigiert. Offener Prüfpunkt aus Runde 1 damit geklärt: **nein**, keine Sortierung, keine Suche.

---

# Runde 5 — Fotos, Backup, Grundriss (Servermodule)

Methodik: `photos.js`, `backup.js`, `floorplan.js` und die zugehörigen Werte aus `config.js` vollständig gelesen. Entgegen der Erwartung mehrere nutzerrelevante Funde.

## U. Fotos — Verarbeitung und Grenzen völlig undokumentiert

Verifiziert gegen [server/photos.js](LuxStage/server/photos.js) und [server/config.js:28-31](LuxStage/server/config.js#L28-L31).

- [x] **Jedes hochgeladene Foto wird verkleinert und neu komprimiert.** — ✅ erledigt (2026-07-26): Tipp-Box in `fotos.md` (DE+EN) ergänzt.
- [x] **Alle Fotos werden in JPG umgewandelt** — ✅ erledigt (2026-07-26): im selben Hinweis ergänzt.
- [x] **Maximale Uploadgröße: 50 MB** — ✅ erledigt (2026-07-26): im selben Hinweis ergänzt.
- [x] **Automatische Drehung nach EXIF** — ✅ erledigt (2026-07-26): im selben Hinweis ergänzt.
- [x] **Zusätzlich entsteht ein Vorschaubild** — ✅ erledigt (2026-07-26): im selben Hinweis ergänzt.
- [x] **Gleichnamige Dateien überschreiben sich.** — ✅ überholt (2026-07-26): Code-Todo 9.1 hat das behoben (`uniqueName()` zählt bei Kollision hoch). Keine Doku-Änderung nötig, Verhalten ist jetzt unauffällig.

## V. `einstellungen.md` — Backup: Verhalten weicht deutlich ab

Verifiziert gegen [server/backup.js](LuxStage/server/backup.js).

- [x] **Fotos werden beim Wiederherstellen ERGÄNZT, nicht ersetzt.** — ✅ erledigt (2026-07-26): in `einstellungen.md` (DE+EN) korrigiert (siehe auch Abschnitt R).
- [x] **Das Backup wird vor dem Einspielen geprüft.** — ✅ erledigt (2026-07-26): in `einstellungen.md` (DE+EN) ergänzt.
- [x] **Konkrete Fehlermeldungen dokumentieren** — ✅ erledigt (2026-07-26): alle drei in `einstellungen.md` (DE+EN) aufgelistet.
- [x] **Maximale Backup-Größe beim Wiederherstellen: 500 MB** — ✅ erledigt (2026-07-26): inkl. Hinweis auf Kommandozeilen-Weg ergänzt.
- [x] **Der Dateiname enthält nur das Datum, nicht die Uhrzeit** — ✅ erledigt (2026-07-26): in `einstellungen.md` (DE+EN) ergänzt.
- [x] **Nur Fotos mit den Endungen jpg, jpeg, png, gif, webp werden zurückgespielt** — ✅ erledigt (2026-07-26): ergänzt.
- [x] **Der Server beendet sich nach der Wiederherstellung selbst** — ✅ erledigt (2026-07-26): bereits in Abschnitt R korrigiert.

## W. Grundriss — Hintergrundbild

Verifiziert gegen [server/floorplan.js](LuxStage/server/floorplan.js).

- [x] **Erlaubte Formate: PNG, JPG, SVG, WebP** — ✅ erledigt (2026-07-26): in `grundriss.md` (DE+EN) ergänzt, inkl. Fehlermeldung.
- [x] **Pro Vorlage ist nur EIN Hintergrundbild möglich.** — ✅ erledigt (2026-07-26): Warnbox in `grundriss.md` (DE+EN) ergänzt.
- [x] **Für das Hintergrundbild gibt es keine Größenbeschränkung und keine Komprimierung** — ✅ erledigt (2026-07-26): in derselben Warnbox ergänzt, inkl. Empfehlung zur Vorbereitung.
- [x] **Der Grundriss wird als PNG-Momentaufnahme für den PDF-Export gespeichert** — ✅ erledigt (2026-07-26): geprüft (Snapshot entsteht bei jeder Änderung und beim Öffnen im Grundriss-Tab, über `emit('change'/'snapshot')` in `FloorplanEditor.vue`). In `export-pdf.md` (DE+EN) erklärt.

## X. EOS-Import — Merge-Dialog erweitert, Health-Badge-Fix, Import-Modal, DMX-Normalisierung

Stand 2026-08-15. Verifiziert gegen [EosMergePreviewDialog.vue](LuxStage/web-app/src/components/EosMergePreviewDialog.vue), [useShowChannels.ts](LuxStage/web-app/src/composables/useShowChannels.ts), [ImportModal.vue](LuxStage/web-app/src/components/show/ImportModal.vue), [dmxAddress.ts](LuxStage/web-app/src/utils/dmxAddress.ts). Abschnitt S (2026-07-26) ist damit überholt — der Merge-Dialog hat inzwischen deutlich mehr Funktionsumfang als die dort beschriebenen drei Gruppen.

- [x] **Merge-Dialog hat jetzt fünf Gruppen statt drei** — ✅ erledigt: „Adresse weicht ab" und „Gerät weicht ab" in `import-eos.md` (DE+EN) ergänzt, inkl. Pfeil-Toggle-Verhalten und Alle/Keine-Buttons.
- [x] **„Neu aktiv"-Kanäle sind einzeln vom Import ausschließbar** — ✅ erledigt: Klick-Verhalten, dauerhafte Persistenz über Importe hinweg und Alle/Keine-Buttons in `import-eos.md` (DE+EN) ergänzt.
- [x] **DMX-Adresse und Gerätebezeichnung werden jetzt aus dem Eos-Export übernommen** — ✅ erledigt: automatische Übernahme bei leerem Feld und Auswahl-Verhalten bei abweichendem Feld in `import-eos.md` (DE+EN) ergänzt.
- [x] **Moving-Light-Erkennung** — ✅ erledigt: neuer Abschnitt in `import-eos.md` (DE+EN) — Fixtures mit Pan/Tilt erhalten automatisch die Notiz „Moving Light".
- [x] **Import-Button öffnet jetzt ein Modal statt eines Dropdowns** — ✅ erledigt: `import-eos.md` (DE+EN) auf den neuen Auswahldialog verwiesen.
- [x] **DMX-Adressfeld wird beim Verlassen automatisch normalisiert** (`normalizeDmxAddress`) — ✅ erledigt: Tipp-Box in `kanaele.md`/`channels.md` (DE+EN) ergänzt, inkl. Beispiel für die Umrechnung über Universumsgrenzen.
- [ ] **Health-Badge-Fix nicht dokumentationsrelevant** — der Bugfix (Summe → Anzahl unterschiedlicher unvollständiger Kanäle) betraf nur die interne Berechnung, nicht die in `kanaele.md`/`channels.md` beschriebene Nutzersicht („Anzahl der Kanäle mit fehlenden Angaben" war schon vorher korrekt formuliert). Kein Doku-Update nötig.
- [ ] **Screenshots veraltet** — `eos-export-dialog.png` und `merge-vorschau.png` zeigen vermutlich noch den alten Export-Dialog (fehlende Aktivierung von „Ziele", „Kanäle", „Geräte") bzw. den alten Merge-Dialog (nur drei statt fünf Gruppen). Neue Screenshots nicht automatisiert erstellbar — manuell nachziehen.

## Priorität (aktualisiert)

0. **N** `installation.md` — die Domain-Angabe im falschen Format lässt die Installation **abbrechen**. Erste Seite, die jeder Self-Hoster liest. Vorgezogen.
0b. **Q** „Fotos pro Druckseite" — Einstellung ohne Wirkung im PDF, an drei Stellen falsch dokumentiert.
0c. **O** Verlauf umfasst keine Fotos/Grundriss und ist auf 50 Versionen begrenzt — Fehlannahme kann Datenverlust bedeuten.
1. **K** Datenschutz — die Aussage „keine Drittanbieter" ist nachweislich falsch, während Bilder an eine externe API gehen. Rechtliches Risiko, nicht nur Doku-Mangel.
2. **J** Widersprüche Doku ↔ App — besonders Login/Benutzername (erster Schritt jedes Nutzers), Farb-Legende und Passwort-Mindestlänge.
3. **I** Offline-Zusage im FAQ — falsche Zusage kann zu Datenverlust führen.
4. **H** Begriffs-Chaos — Doku ist unauffindbar, wenn sie andere Wörter benutzt als der Bildschirm. Idealerweise zuerst die **App** vereinheitlichen (Position/Kategorie), dann die Doku.
5. **A** Registrierung/Login, **I** „Auf alle Shows anwenden".
6. **L** Schnellstart, Glossar, Troubleshooting.
7. **C/D/E/F** dünne Seiten, Screenshots, Umbenennungen, Struktur.

**Anweisung** Nach jedem Punkt einen commit machen ohne Versionserhöhung

---

# Runde 6 — Website-Audit + Stand 2026-09-06

Methodik: `TODO-doku-review.md` und `TODO-webapp-code.md` komplett gelesen. `shared/locales/{de,en}.json` komplett gelesen. Alle vier Website-Root-HTML-Dateien gelesen. `git log --since=2026-08-15` über `web-app/`, `server/`, `shared/locales/` ausgewertet (157 Commits) und Stichproben per Diff/Grep gegen `web-app/src` und `server/` verifiziert.

## Y. Terminologie-Bruch „Kanal" → „Kreis" und „Position" → „Bühnenposition" (App-seitig, seit ca. 2026-08-16/30, unbeachtet)

Seit Commits `3a19ea4`, `c8c47e4`, `ab109f9`, `e2199c7`, `23797d0`, `cefee19` (16.–30.08.2026) verwendet die App-Locale durchgehend „Kreis"/„Kreise" statt „Kanal"/„Kanäle" und „Bühnenposition" statt „Position":

- `shared/locales/de.json:30` `channel.add` = „Kreis hinzufügen" (vorher „Kanal hinzufügen")
- `shared/locales/de.json:49-52` `channel.no_position` = „Ohne **Bühnenposition**", `channel.position.add`, `channel.position.name.placeholder`
- `shared/locales/de.json:140` `field.position` = „**Bühnenposition**" (war laut Runde 2/H „Position")
- `shared/locales/de.json:288-293` `health.*` = „Kreise ohne Adresse", „Kreise ohne Bühnenposition"
- Durchgehend `tab.channels` = „Kreisliste", `show.channels` = „Kreise", `channel.search` = „In Kreisen suchen …"

Kein Recycling von Runde 2/H (dort Position vs. Kategorie, beide gleichzeitig für dasselbe Feld — bleibt erledigt). Betroffene Docs (Stichprobe):

- `docs/de/webapp/kanaele.md:27,31,62,87,89,91,104` — durchgehend „Kanal"/„Kanäle"/„Position"
- `docs/de/features.md` (komplett) — „Kanalliste", „Kanalplan", „Kanäle", „Position" durchgehend
- `docs/de/webapp/index.md:7,8,10,30` — „Kanalplan", „Kanäle"

Website ist bei diesem Wechsel **gespalten**: `index.html`/`i18n.js` verwenden bereits „Kreis(e)" (19 bzw. 41 Vorkommen, 0× „Kanal"), `features.html` dagegen fast durchgehend noch „Kanal" (30× „Kanal", nur 1× „Kreis" an Zeile 213) — Website-interner Widerspruch zwischen Startseite und Feature-Seite.

- [x] Entscheiden: bleibt „Kreis" der App-Standardbegriff? Falls ja, `features.md`/`kanaele.md`/`index.md` (DE+EN) und `features.html` durchgehend auf „Kreis" umstellen; `field.position`/„Bühnenposition" ebenso nachziehen. — ✅ erledigt (2026-09-06): Alle docs/de/**/*.md (Web-App: kanaele.md, index.md, features.md, glossar.md, faq.md, datenschutz.md, einstellungen.md, versionsverlauf.md, shows.md, import-eos.md, import-csv.md, export-csv.md, export-pdf.md, grundriss.md, setup-gestelle.md, setup-zugstangen.md, spielstaette-vorlage.md, info.md, fotos.md, tastaturkuerzel.md, index.md; iOS: einleuchten.md, more.md, osc.md, shows.md, index.md — da `shared/locales` für beide Apps gilt) durchgehend auf „Kreis"/„Kreise"/„Bühnenposition" umgestellt, außer wo „Position" eine andere Bedeutung hat (Klick-Koordinate auf Zugstange, CSV-Spaltennummer). Sidebar-Eintrag in `config.js` (DE) „Kanäle"→„Kreise". `features.html` DE-Text ebenfalls umgestellt (siehe unten). EN-Docs und `index.html`/`i18n.js` unverändert, da EN-App-Locale weiterhin „channel"/„Position" sagt.
- [x] EN-Locale prüfen: `en.json:140` `field.position` = „Position" (nicht „Stage Position") — DE/EN sind hier bereits wieder asymmetrisch benannt, zusätzlich zum Kanal/Kreis-Wechsel. — ✅ geprüft (2026-09-06): bestätigt, EN-Locale weiterhin „channel"/„Position", deshalb EN-Docs bewusst nicht geändert (siehe oben).

## Z. Netzwerk-Ansicht — komplett neues Feature, weder in Docs noch auf der Website

Commits `a628071` (29.08., „Netzwerkansicht hinzufügen: Geräte, Switches, Räume mit Positionierung"), `c0be3b2`/`cb0de4c` (überarbeitet). Verifiziert:

- `web-app/src/router/index.ts:52-56` — eigene Top-Level-Route `/network` → `NetworkView.vue`, gleichrangig mit Shows/Archiv/Vorlagen.
- `web-app/src/App.vue:324-327` — `nav.network` ist ein fünfter Sidebar-Eintrag neben Shows, Archiv, Vorlagen (Einstellungen separat).
- `shared/locales/de.json:342-372` — ca. 30 `network.*`-Keys: Elemente (Dose/Gerät/Switch), Verbindungen, Räume, PDF-Export, Auto-Anordnen, Vollbild.

In **keiner** Docs-Seite und **keiner** Website-Seite erwähnt oder beworben:

- `docs/de/webapp/index.md:17-24` — Navigationstabelle nennt nur „vier Symbole"; tatsächlich sind es jetzt **fünf**.
- `docs/de/features.md` — keine Netzwerk-Sektion.
- `luxstage-website/features.html:41-51` — Feature-Navigation hat keinen Netzwerk-Anker; Sektionsliste endet bei „Benutzerverwaltung".

Nicht identisch mit dem offenen Punkt in B („vier Symbole", dort wegen Login/Registrierung) — hier fehlt ein ganzes neues Feature komplett.

- [x] Neue Docs-Seite `webapp/netzwerk.md` (DE+EN) anlegen, Sidebar-Zahl korrigieren. — ✅ erledigt (2026-09-06): `docs/de/webapp/netzwerk.md` und `docs/en/webapp/network.md` neu angelegt (Elemente, Topologie, Verbindungen/Port-Grid, Elemente-Tabelle, PDF-Export, Sperrung). In `docs/de/webapp/index.md` und `docs/en/webapp/index.md` „vier"→„fünf Symbole", Netzwerk-Zeile in Navigationstabelle und „Einstieg"-Liste ergänzt. Sidebar-Eintrag in `config.js` (DE+EN) ergänzt.
- [x] Feature-Sektion auf Website (`features.html`) und/oder `docs/de/features.md` ergänzen, falls öffentlich beworben werden soll. — ✅ erledigt (2026-09-06): Neuer Abschnitt „Netzwerk-Dokumentation" in `docs/de/features.md` und `docs/en/features.md` ergänzt. `luxstage-website/features.html`: neue Sektion `#netzwerk` (Topologie, Port-Grid, Räume & Suche, PDF-Export) plus Nav-Anker „Netzwerk" ergänzt.

## AA. Circuit-Scan (KI-Foto-Scan) — Rückkehr des als „entfernt" dokumentierten OCR-Features, Datenschutztext dadurch wieder falsch

Runde 1/K hatte bestätigt, dass das OCR-Feature (Foto-Scan per Anthropic/Claude) nicht mehr existiert, Datenschutzaussage „keine Kommunikation mit Drittanbietern" deshalb korrekt. Seit Commit `cefee19` (30.08., „Circuit-Scan-Funktion …") **nicht mehr zutreffend**:

- `server/circuit-scan.js:1-6` — liest Kreisliste per Claude Vision aus, importiert `@anthropic-ai/sdk`, Modell `claude-sonnet-5`.
- `server/circuit-scan.js:33-40` — `defaultAnthropicClient()` instanziiert echten Anthropic-Client.
- `shared/locales/de.json:311-322` — `import.modal.scan.*`: „Foto des ausgefüllten Kreislisten-Vordrucks hochladen — Filter, Notizen und neue Kreise werden per KI ausgelesen."

Direkter Rückfall auf den in K behandelten Sachverhalt — als **neuer** Fund zulässig, weil sich der Code-Zustand seither geändert hat (Feature kam zurück):

- `docs/de/datenschutz.md:9` sagt unverändert: „Es findet keine Kommunikation mit Servern von Drittanbietern statt." — jetzt für die Web-App **falsch**.
- Feature funktional nirgends dokumentiert (`import-csv.md`, `import-eos.md` behandeln nur die zwei alten Importwege).
- Website erwähnt das Feature ebenfalls nicht.

- [x] `datenschutz.md` (DE+EN) um Web-App-Fall Circuit-Scan ergänzen: Bilder gehen bei Nutzung an die Anthropic-API. — ✅ erledigt (2026-09-06): Überblick-Absatz in `docs/de/datenschutz.md`/`docs/en/privacy.md` nennt die Ausnahme explizit, neuer Abschnitt „Kreisliste scannen (KI-Foto-Scan)" / „Scan Channel List (AI Photo Scan)" erläutert Umfang, Zweck und Link zu Anthropics Datenschutzbestimmungen.
- [x] Neue Doku-Seite/Abschnitt für „Kreisliste scannen" (dritter Importweg neben CSV und EOS). — ✅ erledigt (2026-09-06): Neue Seiten `docs/de/webapp/scan-kreisliste.md` und `docs/en/webapp/scan-channel-list.md` (Vordruck, Upload, Vorschau mit einzeln abwählbaren Zeilen, Übernehmen). Verlinkt von `webapp/index.md` (DE+EN) und `import-csv.md` (DE+EN); Sidebar-Eintrag in `config.js` (DE+EN) ergänzt; „Import & Export"-Sektion in `features.md` (DE+EN) um den Scan ergänzt.
- [x] Rechtliches Risiko wie ursprünglich in K eingestuft — jetzt wieder akut. — ✅ geprüft (2026-09-06): `luxstage-website` (index.html, i18n.js, impressum.html) macht keine eigene Datenschutzaussage zu Drittanbietern/Anthropic — nur Links zur Doku-Datenschutzseite. Keine Website-Änderung nötig.

## AB. Benutzerrollen entfernt — Docs und Website behaupten weiterhin zwei Rollen mit unterschiedlichen Rechten

Commit `0133812` („Benutzerrollen entfernen: keine Unterscheidung mehr zwischen Admin und Techniker", 24.08.). `server/db/users.js` enthält kein `role`-Feld mehr. `shared/locales/de.json:548-549` behält noch `settings.users.role.admin`/`role.techniker` als Locale-Rest (nicht tiefer verifiziert, ob im Frontend noch aufgerufen).

Betroffen, alle noch mit Zwei-Rollen-Modell:

- `docs/de/webapp/einstellungen.md:116-121,139` — Rollentabelle admin/Techniker mit unterschiedlichen Rechten.
- `docs/de/features.md:157-164` — Abschnitt „Benutzerverwaltung", Tabelle admin/techniker mit Rechteunterschied.
- `docs/de/faq.md:27` — „Admins und Techniker können gleichzeitig arbeiten."
- `luxstage-website/features.html:399,415-421` — „Zwei Rollen, klare Grenzen: Techniker arbeiten, Admins verwalten", `tech_no1`/`tech_no2`.
- `luxstage-website/i18n.js:282,285` — dieselbe Aussage in den Locale-Strings.

Nicht identisch mit dem offenen Prüfpunkt in G/Runde 1 (ging von Existenz zweier Rollen aus, wollte nur Rechte-Details klären) — hier existieren Rollen laut Code **gar nicht mehr**.

- [x] Falls Rollenentfernung endgültig: Rollentabellen in `einstellungen.md`, `features.md`, `faq.md` (DE+EN) und `features.html`/`i18n.js` überarbeiten. — ✅ erledigt (2026-09-06): `einstellungen.md`/`settings.md` — Rollentabelle entfernt, neutraler Text „keine Benutzerrollen, jeder Benutzer hat vollen Zugriff". `features.md` — Abschnitt „Benutzerverwaltung" auf „Einfache Zugänge für dein Team" umgeschrieben. `faq.md` — „Admins und Techniker" durch rollenneutrale Formulierung ersetzt. `features.html` — Zwei-Karten-Layout (Admin/Techniker) auf „Jeder Benutzer kann" / „… und außerdem" umgestellt, Headline/Beschreibung angepasst. `i18n.js` (DE+EN) — dieselben Strings (`sec_users_headline`, `sec_users_desc`, `role_admin`, `role_tech`) korrigiert.
- [x] Klären, ob `settings.users.role.admin`/`role.techniker` in der App tatsächlich noch angezeigt werden (Code-seitige Nachprüfung nötig). — ✅ geprüft (2026-09-06): `grep role` über `web-app/src` zeigt keinen Aufrufer dieser Keys und kein `requireAdmin` mehr in `server/`. Bestätigt: keine Rechteunterschiede zwischen Benutzern mehr, die beiden Locale-Keys sind tot.

## AC. Übrige Prüfpunkte A–E ohne neuen Befund

- **A**: Keine erfundenen Website-Features gefunden — alle beworbenen Funktionen (EOS-Import, PDF-Export, Grundriss, Versionsverlauf, Fotos, Spielort-Vorlagen, Echtzeit-Sync) existieren im Code. Fehlende Bewerbung: Netzwerk-Ansicht (Z) und Circuit-Scan (AA).
- **C**: Netzwerk-Ansicht und Circuit-Scan sind in beiden (Docs + Website) nicht nachgezogen — siehe Z, AA. Rein interne Änderungen (Multi-Tenant, JWT-Härtung, Rate-Limiting, Refactorings) sind zu Recht nicht dokumentiert.
- **D**: Über Y, Z, AA, AB hinaus keine weiteren Abweichungen in den geprüften Kernseiten.
- **E**: Kein weiterer Widerspruch außer der unter Y beschriebenen Kanal/Kreis-Spaltung zwischen `index.html` und `features.html`.

## AD. Rechtliche Seiten (Datenschutz, Impressum) von Docs auf Website verlagert

Anlass: `docs.luxstage.app/de/datenschutz` war nicht aufrufbar (nginx im Docs-Container hatte keine Clean-URL-Regel für `.html`-lose VitePress-Routen — siehe `nginx.conf`/`Dockerfile` in `luxstage-docs`). Statt nur den nginx-Fehler zu fixen, auf Wunsch strukturell bereinigt: Datenschutz gehört inhaltlich zum rechtlichen Rahmen des Betreibers (wie das Impressum), nicht zur Produktdokumentation.

- [x] Vollständiger Datenschutztext von `docs/de/datenschutz.md`/`docs/en/privacy.md` nach `luxstage-website/datenschutz.html`/`privacy.html` verschoben (Stil an `impressum.html` angeglichen, inkl. Circuit-Scan-Abschnitt aus Runde 6/AA).
- [x] Docs-Seiten auf einen Verweis reduziert, VitePress-Nav/Footer (`config.js`, DE+EN) zeigen jetzt direkt auf `luxstage.app/datenschutz.html`/`privacy.html`.
- [x] Website-Footer (`index.html`, `features.html`) verlinkt sprachabhängig über neues `data-i18n-href-privacy`-Attribut in `i18n.js` auf die passende Datei; `impressum.html`-Footer ebenfalls auf lokale Datei umgestellt.
- [x] `nginx.conf` (neu) mit `try_files`-Fallback ergänzt und im `Dockerfile` eingebunden, damit clean URLs (`/de/xyz` ohne `.html`) im nginx-Produktionsbuild grundsätzlich funktionieren — unabhängig von der Verlagerung, behebt die eigentliche Fehlerursache für alle übrigen Docs-Seiten.