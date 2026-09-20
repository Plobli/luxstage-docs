# Anmeldung

## Anmelden

Beim Aufruf der Web-App erscheint die Login-Seite mit zwei Feldern:

- **E-Mail-Adresse** – dein Login-Name
- **Passwort**

Klick auf **„Anmelden"**. Bei falschen Zugangsdaten erscheint „Anmeldung fehlgeschlagen. Bitte E-Mail-Adresse und Passwort prüfen."

**Zu viele Versuche:** Nach 10 fehlgeschlagenen Login-Versuchen innerhalb von 15 Minuten sperrt der Server für die betreffende IP-Adresse mit der Meldung „Zu viele Versuche. Bitte warten." — danach 15 Minuten warten bevor ein neuer Versuch möglich ist.

## Registrierung

Unterhalb des Anmelde-Formulars erscheint der Link **„Noch kein Konto? Registrieren"**. Bei einem gehosteten Team unter [luxstage.app](https://luxstage.app) läuft die Registrierung über ein Team-Kürzel plus E-Mail-Adresse und Passwort, per Bestätigungslink per E-Mail (Double-Opt-in). Neue Teammitglieder eines bestehenden Teams legt man stattdessen über **Einstellungen → Benutzerverwaltung → Neuer Benutzer** an (siehe [Einstellungen](./einstellungen)).

## Passwort vergessen

Unterhalb des Anmelde-Formulars steht der Link **„Passwort vergessen?"**:

1. Klick auf den Link → E-Mail-Adresse eingeben → **„Link anfordern"**
2. Aus Sicherheitsgründen erscheint immer derselbe Hinweis, unabhängig davon, ob ein Konto mit dieser Adresse existiert: „Falls ein Konto mit {E-Mail} existiert, haben wir einen Link zum Zurücksetzen verschickt."
3. Der Link in der E-Mail ist **1 Stunde** gültig und führt zu einer Seite zur Vergabe eines neuen Passworts (mindestens 8 Zeichen, mit Bestätigung)

::: tip Self-Hosting ohne SMTP
Betreibst du LuxStage selbst und hast keinen Mailversand (SMTP) eingerichtet, entfällt dieser Link — siehe [Einstellungen für Self-Hosting](./einstellungen-self-hosting).
:::
