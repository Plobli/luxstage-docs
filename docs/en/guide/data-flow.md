# Who enters what, and where it shows up

All data of a show lives in one place: your LuxStage server. The web app, desktop app, iOS and Android apps are just different windows onto the same show. What you enter in one place, all others see after the next sync.

<div class="datenfluss">
<svg viewBox="0 0 720 300" role="img" aria-label="Input from the web app, desktop app, iOS and Android flows into the show on the server. From there it appears in the apps, the PDF lighting plan, the CSV export and the venue template.">
  <g class="df-box">
    <rect x="10" y="30" width="190" height="52" rx="10"/><text x="105" y="61">Web app · Desktop</text>
    <rect x="10" y="124" width="190" height="52" rx="10"/><text x="105" y="155">iPhone · iPad</text>
    <rect x="10" y="218" width="190" height="52" rx="10"/><text x="105" y="249">Android</text>
  </g>
  <g class="df-core">
    <rect x="265" y="100" width="190" height="100" rx="14"/>
    <text x="360" y="143">Your show</text>
    <text x="360" y="167" class="df-sub">on the LuxStage server</text>
  </g>
  <g class="df-box">
    <rect x="520" y="10" width="190" height="52" rx="10"/><text x="615" y="41">All apps</text>
    <rect x="520" y="86" width="190" height="52" rx="10"/><text x="615" y="117">PDF lighting plan</text>
    <rect x="520" y="162" width="190" height="52" rx="10"/><text x="615" y="193">CSV export</text>
    <rect x="520" y="238" width="190" height="52" rx="10"/><text x="615" y="269">Venue template</text>
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

You can enter almost everything everywhere. The tables below list the exceptions and show where a field appears later.

## Three notes, three purposes

This is where most misunderstandings happen:

| Note | Purpose | Where visible |
|---|---|---|
| **Lighting note** (on the channel) | What to do when focusing, e.g. “on sofa, soft”. This is the focus note. | all apps, PDF lighting plan, CSV |
| **Caption** (on the photo) | What the picture shows | all apps, PDF below the photo |
| **Personal annotation** (on the channel) | Your own reminder | only you, in all apps. Never in PDF or CSV |

::: tip Rule of thumb
If the whole team needs to know something while focusing, it belongs in the **lighting note**. The photo caption only explains the picture.
:::

You can mark a lighting note as a **hint** (e.g. “turn away”). It then is a task instead of a focus point, see [Channels](/en/webapp/channels#mark-a-note-as-a-hint).

## Channels

| Field | Enter | Appears in |
|---|---|---|
| Channel, address, fixture | everywhere | apps, PDF, CSV, template |
| Stage position | everywhere | apps, PDF (as group title), CSV, template |
| Gel and 2nd gel | everywhere | apps, PDF (also towers, installation spots, rigging), CSV, template |
| Lighting note | everywhere | apps, PDF (only channels with a note), CSV, template |
| Hint marker | everywhere | apps, CSV. Not in the PDF |
| Quantity | everywhere | apps, PDF (from 2), CSV, template |
| Priority | everywhere | apps, PDF (as badge), CSV |
| Personal annotation | everywhere | only you |
| Focus checkmarks | everywhere | apps |
| Channel groups | everywhere | apps, template |
| Mounting | set automatically when you place a fixture in the rigging | web app |

## Photos

| Field | Enter | Appears in |
|---|---|---|
| Photo, order | everywhere | apps, PDF |
| Caption | everywhere | apps, PDF (single line, shortened) |
| Assigned channels | everywhere | apps, PDF (“Channels: 12, 14” below the photo) |

## Setup notes, rigging, side towers, installation spots

You enter all fields of these areas everywhere. They appear in all apps and in the PDF lighting plan.

- **Rigging:** name, batten number, length, height, type, note per batten; per fixture channel, position and note. A fixture linked to a channel takes fixture type and gel from the channel.
- **Side towers:** name, number of slots, note per tower and per slot.
- **Installation spots:** name, type, location, hint and assigned channels. A channel belongs to at most one spot.
- **Setup notes:** headings, text and table rows.

## Show data

| Field | Enter | Appears in |
|---|---|---|
| Name, date | everywhere | apps, PDF |
| Season | everywhere | apps, PDF header |
| Venue | web app: only when creating. Apps: any time | apps, PDF |
| Areas (rigging, towers, 2nd gel) on/off | everywhere | apps, PDF |
| Archived | everywhere | apps |

## Web app only

- **[Import from EOS](/en/webapp/import-eos)** and **[Import CSV](/en/webapp/import-csv)**. In the EOS import you choose which console fields go into the lighting note. All other console fields are only visible in the web app when hovering over the fixture.
- Editing the **[venue template](/en/webapp/venue-template)**. The apps use the template when creating a show.

## What the venue template carries over

A template brings the fixed equipment of a venue into every new show:

- Channels with address, fixture, stage position, gel, 2nd gel, lighting note and quantity
- Channel groups and installation spots
- Rigging with fixtures, and side towers
- Setup notes: headings and table rows, texts start empty

Not in the template: priority, hint marker, season and anything personal. These belong to the individual show.

The template PDF is a blank form: channel, address and fixture are printed, the rest is left free to fill in.
