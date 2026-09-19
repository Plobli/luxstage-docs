# Login

## Signing in

When you open the web app, the login page shows two fields:

- **Email address** – your login name
- **Password**

Click **"Sign in"**. On incorrect credentials, the message "Login failed. Please check email address and password." appears.

## Registration

Below the sign-in form, the link **"No account yet? Register"** appears. On a hosted team at [luxstage.app](https://luxstage.app), registration works via a team slug plus email address and password, confirmed by an email link (double opt-in). New members of an existing team are instead created via **Settings → User Management → New user** (see [Settings](./settings)).

## Forgot password

Below the sign-in form is the **"Forgot password?"** link:

1. Click the link → enter your email address → **"Request link"**
2. For security reasons, the same message always appears, regardless of whether an account with that address exists: "If an account with {email} exists, we've sent a reset link. Please check your inbox."
3. The link in the email is valid for **1 hour** and leads to a page for setting a new password (at least 8 characters, with confirmation)

::: tip Self-hosting without SMTP
If you self-host LuxStage and haven't set up email delivery (SMTP), this link is not shown — see [Settings for Self-Hosting](./settings-self-hosting).
:::
