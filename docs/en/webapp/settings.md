# Settings

**Settings** are accessible via the gear icon (⚙️) in the left sidebar.

::: tip Hosted team (luxstage.app)
On a hosted team at [luxstage.app](https://luxstage.app), the operator manages server operation, email delivery, backups, and updates centrally. That's why the sidebar there only shows **Account**, **Display**, and **User Management**. If you self-host LuxStage, you also see **Backup**, **Server**, **Email / SMTP**, and **Update** — see [Settings for Self-Hosting](./settings-self-hosting).
:::

---

## Account

**Change password**

Change the password for your account:

1. Enter **current password**
2. Enter **new password**
3. **Confirm new password**
4. Click **"Change password"**

---

**Photos per print page**

Specifies how many photos fit on an A4 page — applies equally to browser printing and PDF export.

- Options: 1, 2, 4, 6, 8, 9, 12

---

**Sign out**

Clicking **"Sign out"** ends the current session.

---

## Display

**Language**

Select the display language of the app:

- **German**
- **English**

Click on the desired option – the app switches language immediately.

---

**Unit**

Unit for lengths and heights on bars:

- **m**, **cm**, or **mm**

---

## User Management

**Users**

List of all existing users in your team with email address and a source badge. LuxStage has no separate user roles — every invited user has the same permissions.

The badge shows the user's source:

| Source | Description |
|--------|-------------|
| **DB** | Self-created or self-registered – can be deleted |
| **Env** | Configured via environment variable (self-hosting only) – cannot be deleted |

Only users with source **DB** have a **"Delete"** button.

---

**New user**

Creates a new user for your team. The initial password is generated automatically and sent by email.

1. Enter **email address**
2. Click **"Create"**

---

**Reset password**

Resets a user's password and displays the new temporary password.

1. Enter the user's **email address**
2. Click **"Reset"**
