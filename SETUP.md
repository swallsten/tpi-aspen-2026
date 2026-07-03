# TPI Aspen Forum 2026 — hosting + Wix setup (070226)

## Part 1. Host the folder on GitHub Pages (about 10 minutes)

1. github.com → New repository → name it `tpi-aspen-2026`, Public → Create.
2. "uploading an existing file" link → drag EVERYTHING in this folder in
   (the html files and the assets folder together) → Commit.
3. Repo Settings → Pages → Source "Deploy from a branch" → Branch `main`,
   folder `/ (root)` → Save. Wait ~2 minutes.
4. Your pages are now live at
   your GitHub Pages URL etc.
   Open a few to confirm.

One extra file. Drop the seventeen-year poster PDF (v6) into the assets
folder named exactly `tpi-17-years.pdf` so the download link on Past Forums
works. Upload it to the repo's assets folder the same way.

## Part 2. Wix pages (about 40 minutes)

Create or rename pages so the URL slugs match EXACTLY (the nav links inside
the embeds point at these):

| Wix page (slug)    | Embed this URL                       | Start height |
|--------------------|--------------------------------------|-------------|
| `/` (home)         | .../index.html                       | 7200 px |
| `/about`           | .../about.html                       | 2800 px |
| `/agenda`          | .../agenda.html                      | 8200 px |
| `/speakers`        | .../speakers.html                    | 5200 px |
| `/travel`          | .../travel.html                      | 3400 px |
| `/past-forums`     | .../past-forums.html                 | 2600 px |
| `/adjourned`       | .../adjourned.html                   | 3400 px |
| `/seventeen-years` | .../seventeen-years.html             | 3600 px |
| `/register`        | build natively in Wix (see below)    | n/a |

Per page: Add (+) → Embed Code → "Embed a site" → paste the URL → stretch
the element full width and set the height from the table → check Preview and
nudge the height until the footer sits right. Too tall is fine (the overflow
blends into the dark footer color); too short clips.

Keep the Wix header and footer EMPTY or delete their contents. The design
includes its own header, nav, and footer inside each page.

SEO panel per page (Page settings → SEO): copy the title and description
from the top of each html file (the `<title>` and `<meta name="description">`
lines).

## Part 3. Register page (native Wix)

Build the rate cards as plain Wix text and buttons using
`Reference Pages/TPI Register.dc.html` as the visual guide, then add the
Wix Events / "Sell Tickets" app with the two ticket types,
Corporate/Trade $3,750 and Academic/Gov/Nonprofit $1,500. This is the only
page you build by hand, and it is the simplest one.

## Mobile

Built in. Every embedded page is responsive at phone widths (hamburger menu,
sticky bottom Register bar, single-column layouts, horizontal-scroll chips).
Do NOT restyle these pages in Wix's mobile editor; just make sure the embed
element itself is full-width on mobile too.

## Open items carried over from review

- Subscribe button in the footer is decorative. Newsletter signup URL still needed to wire the Subscribe button. Send the
  URL and it takes one line to wire up.
- Confirm the ~8 unverified speaker bios and the pending-ethics-approval
  names (Lin, Schwarz) before publish.
- Confirm the gondola photo credit on the Adjourned page.
