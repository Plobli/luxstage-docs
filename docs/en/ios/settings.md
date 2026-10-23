# Settings (iOS)

**Settings** are accessible via the tab of the same name in the global tab bar (from the shows overview, not within a show).

<img src="/img/ios/einstellungen.png" alt="Settings" class="ios-screenshot">

**Team** and **Setup** come first, followed by the subpages **Remote connection** and **Diagnostics**.

## Team

Shows your current team. **Change team** signs you in to another team directly, without signing out first. The setting applies to GridDeck and Shows.

## Language

Use the **Language** menu to select the display language of the app (German or English).

## Remote connection

The **Remote connection** subpage holds the venues. The list is stored **locally on the device**. Server suggestions (login required) can be added with a tap, and you can add your own venues with a name and IP. Tapping a venue makes it the active connection for the whole app.

The **Eos control** section contains:

- **Eos User** — stepper (−1 to 99). The value applies device-wide, is saved immediately and survives app restarts and updates. Changing it reconnects the app automatically.
- **Quick At key** — stepper (5 to 100 %, in steps of 5, default 80 %). Sets the level the quick key in the Remote tab applies to the selected channels. The value applies to this device; when you are signed in, it is also saved to your LuxStage account and picked up on your other devices.

::: warning Using the ETC RFR app too
If you also use the ETC RFR app, pick a **different Eos user** there than in LuxStage, otherwise the two apps interfere with each other.
:::

## Diagnostics

The **Diagnostics** subpage also shows the app version and build. Optionally, and only with your consent, the app sends crashes and an anonymous connection log (connection and app states such as standby or network changes, no show content). **Send log now** transmits the log immediately, e.g. for support.

## Restart setup

Runs the setup assistant again. If a sign-in or venue already exists, cancel it with the **X** at the top.

## Sign out

The **Sign out** button ends the session and returns directly to the shows.
