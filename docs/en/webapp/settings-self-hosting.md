# Settings for Self-Hosting

These tabs only appear if you self-host LuxStage (not on a hosted team at [luxstage.app](https://luxstage.app)) — there, the operator manages server operation, email delivery, backups, and updates centrally. The remaining tabs (Account, Display, User Management) are described under [Settings](./settings).

::: tip Update notification
If a server update is available, a small dot on the Settings icon in the sidebar indicates it.
:::

---

## Login without SMTP

If no email delivery (SMTP) is configured when self-hosting, the "Forgot password?" link on the login page disappears. Instead, the message "Contact your administrator to reset your password." appears. An admin can set a new password under **User Management → Reset password** (see [Settings](./settings)).

---

## Backup

::: tip Sensitive data in the backup
The ZIP backup contains the complete database, including password hashes for all users — store it accordingly carefully.
:::

**Create backup**

Downloads all show data as a ZIP archive. The filename only contains the date (e.g. `luxstage-backup-2026-07-25.zip`), not the time — two backups on the same day have identical names and overwrite each other in the download folder.

- Click **"Download ZIP backup"**
- The download starts automatically

---

**Restore backup**

Restores all show data from a previously created ZIP backup. Photos are **added, not replaced** — existing photos with no counterpart in the backup remain in place. The server shuts itself down after restoring and only restarts automatically if a process manager (e.g. PM2, the default for self-hosting) is supervising it.

1. Click **"Select ZIP file …"**
2. Choose a ZIP backup file from the file system
3. Click **"Restore"**
4. Confirm the confirmation dialog

::: warning Note
The database (shows, channels, sections) is completely replaced by the backup. Photos are only added — photos missing from the backup remain in place.
:::

The backup is validated before restoring: whether the ZIP contains a valid database, and whether it's undamaged. If validation fails, the current state remains **untouched**. Possible error messages:

- "ZIP does not contain luxstage.db"
- "Database is corrupted or invalid"
- "Upload too large" — maximum backup size for restoring: **500 MB**. Larger data sets can only be restored via the command line on the server.

Only photos with the extensions `jpg`, `jpeg`, `png`, `gif`, `webp` are restored — other file types in the ZIP are silently skipped.

---

## Server

| Field | Description |
|-------|-------------|
| **Server URL** | API server address (default: http://localhost:3000). Takes effect **immediately** when leaving the field, with no save button — a typo can make the app unusable. |
| **App version** | Currently installed app version |
| **Server version** | Currently installed server version |
| **Disk (free)** | Available storage space on the server — only shown when the server is reachable. Otherwise a connection error is shown instead. |

---

## Email / SMTP

SMTP configuration for automatic emails (welcome, password reset):

| Field | Description | Default |
|-------|-------------|---------|
| **SMTP host** | Mail server hostname | mail.example.com |
| **Port** | SMTP port | 587 |
| **TLS (port 465)** | Checkbox for TLS encryption | – |
| **Username** | SMTP login name | – |
| **Password** | SMTP password | – |
| **Sender (From)** | Sender address | LuxStage <noreply@example.com> |

::: tip Saved password
A previously saved SMTP password is never displayed for security reasons — the field stays empty, with only a placeholder (••••••••) indicating one is set. Saving without filling in the field keeps the old password.
:::

**Buttons:**
- **"Save"** – Save settings
- **"Send test email"** – Opens a dialog to enter the recipient address (pre-filled with your own email), then sends a test email to verify the configuration

---

## Update

Checks for new versions and updates the server. If an error occurs, the old state is automatically restored.

1. Select a **release** — the list comes from the project's GitHub releases, with the newest entry preselected. The update check starts automatically when opening the tab or switching releases.
2. If an update is available, the page shows the release name and its release notes as a changelog. Without an available update, the **"Update now"** button is disabled.
3. Clicking **"Update now"** starts the update. A progress bar and a live terminal log show the process in real time.
