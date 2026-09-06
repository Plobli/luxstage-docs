# Privacy Policy

*Last updated: July 2026*

This privacy policy applies to both the **iOS app** and the **web app**, regardless of whether you self-host LuxStage or use it as a hosted service at [luxstage.app](https://luxstage.app).

## Overview

LuxStage is designed to **collect no personal data**. Both apps communicate exclusively with the LuxStage server — with self-hosting, your own server; with the hosted service, the operator's server. There is no communication with third-party servers — **with one exception:** if you use the "Scan channel list" feature in the web app, the photo you upload is sent to Anthropic's API (see the [Scan Channel List (AI Photo Scan)](#scan-channel-list-ai-photo-scan) section below).

## Web app and self-hosting

The web app runs in the browser and stores only the server address and the selected display language locally (`localStorage`). Show data (channel plans, photos, floor plans, user accounts) is processed and stored exclusively on the LuxStage server.

With **self-hosting**, you are the responsible data controller under GDPR and are yourself responsible for data security, access protection, and any data processing agreements (e.g. with a hosting provider for the server).

With the **hosted service** (luxstage.app), the LuxStage operator is the responsible party for data stored there.

## Scan Channel List (AI Photo Scan)

Under "Import", the web app offers a **"Scan channel list"** feature: a photo of a filled-out channel list (printed template or handwritten) is uploaded so that filters, notes, and new channels can be read automatically.

For this feature, the uploaded photo is sent to the **Anthropic API** (Claude Vision, the provider of the underlying AI model) and processed there for text recognition. This is the only exception to the rule that LuxStage communicates exclusively with your own LuxStage server.

- The transfer only happens when you actively use the "Scan channel list" feature.
- No other show or user data is sent to Anthropic — only the selected photo and, as a reading aid, the channel data already stored in the show (channel number, address, fixture, position).
- The result is shown in a preview where you can deselect each detected change individually before it is applied.
- [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy) applies to this processing.

If you don't use this feature, nothing changes for you — the other ways of building a channel list (manual entry, EOS import, CSV import) communicate exclusively with your own LuxStage server.

## What data is stored?

### Locally on your device

The iOS app stores only the following data locally on your device:

- **Server URL** — the address of your self-hosted LuxStage server
- **EOS User ID** — a device-specific setting for OSC control (number 1–99)
- **Language preference** — the selected display language of the app

The app itself does not transmit this data to the app developer or any third party.

### On your own server

The iOS app transfers show data (channel plans, photos, floor plans) exclusively with the LuxStage server you operate yourself. What data is stored there is entirely under your control. You are responsible for data security on your own server.

## Data collection by Apple

When downloading the app from the App Store, [Apple's Privacy Policy](https://www.apple.com/privacy/) applies. Apple may collect diagnostic data and purchase information as part of App Store operations. This data is managed by Apple and is not shared with the app developer.

## Analytics & Tracking

The LuxStage app contains **no tracking**, **no analytics libraries**, and **no advertising**. No usage data is transmitted to the app developer.

## Camera and Photos

The app can — with your permission — access your **camera** and **photo library** to add photos to a show. These photos are uploaded exclusively to your own LuxStage server and are not forwarded to any third party.

## Network access

The app connects to the following destinations:

- **Your LuxStage server** (local network or your own VPS) — for show data, real-time synchronisation, and OSC commands
- **Your EOS lighting console** (local network) — for OSC control commands

There is no connection to external servers of the app developer or third parties.

## App Store – Privacy Labels (App Privacy)

The following information is provided in the App Store:

| Category | Collection | Purpose |
|----------|------------|---------|
| Purchase history | By Apple | App Store operations |
| Device identifiers | None | – |
| Usage data | None | – |
| Diagnostics | None | – |
| Contact info | None | – |
| Photos | Optional, local | Only to your own server |

**Data Not Linked to You** — no data is linked to your identity or shared with third parties.

## Legal Notice

The legal notice (Impressum) for the hosted service luxstage.app can be found at [luxstage.app/impressum.html](https://luxstage.app/impressum.html).

## Changes to this Privacy Policy

Changes will be published on this page. The date of the last update is shown at the top.

## Contact

For privacy-related questions:

- Email: [hello@luxstage.app](mailto:hello@luxstage.app)
- GitHub: [github.com/Plobli/LuxStage](https://github.com/Plobli/LuxStage)
