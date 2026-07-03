# Letting someone edit speakers and the agenda (one-time setup)

Date: July 3, 2026

The site can read its speakers and agenda from a Google Sheet, so a non-technical
person edits a spreadsheet and the website updates itself. Until you finish the
steps below, the site keeps showing the built-in data, so nothing breaks in the
meantime. Setup is about fifteen minutes and you only do it once.

## What you have
`tpi-aspen-data.xlsx` is the starter spreadsheet, already filled with all 55
speakers and all 31 sessions, on two tabs named Speakers and Agenda.

## Step 1. Turn it into a Google Sheet (5 min)
1. Go to drive.google.com and upload `tpi-aspen-data.xlsx`.
2. Double-click it, then File, Save as Google Sheets. That creates a real Google
   Sheet with the two tabs. You can delete the uploaded .xlsx afterward.
3. Rename it something obvious like "TPI Aspen 2026 site data."

## Step 2. Publish the two tabs as CSV (5 min)
This is what lets the website read the data. It does not make the sheet editable
by the public, only readable by the site.
1. In the sheet, File, Share, Publish to web.
2. In the dialog, choose the Speakers tab (not "Entire document"), and choose
   Comma-separated values (.csv) as the format. Click Publish. Copy the link it
   gives you.
3. Do the same again for the Agenda tab. Copy that link too.
You now have two links, one for Speakers and one for Agenda.

## Step 3. Point the site at the sheet (2 min)
1. In your GitHub repo, open `config.js` and click the pencil to edit.
2. Paste the two links between the quotation marks:
   speakersCsvUrl: "the Speakers link",
   agendaCsvUrl: "the Agenda link"
3. Commit changes. The site now reads from the sheet within a few minutes.

## Step 4. Give your editor access (2 min)
In the sheet, click Share and give the person Editor access. That lets her change
the data. She never needs GitHub, Wix, or anything else.

## How to confirm it worked
1. Paste the Speakers CSV link into a browser. It should download or show a
   spreadsheet-looking text file. If it shows a Google login screen instead,
   the publish step did not take; redo Step 2.
2. Open the live Speakers page, then open the browser's developer console
   (right-click, Inspect, Console). You should see "TPI speakers source: sheet".
   If it says "fallback" or "built-in", the link is missing or wrong in config.js.
3. Make a tiny test edit in the sheet (add a period to a bio), wait about five
   minutes, reload the page. The change should appear.

## Two things worth knowing
- There is a cache. Edits show up on the site within roughly five minutes, not
  instantly. Tell your editor so she does not think it failed.
- Anyone with Editor access to the sheet can change the live site, so keep that
  sharing list short.
