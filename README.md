# Mileage Log

A small web app for logging work drives. Enter where you went, and it works out the driving distance from your office to each place and back, then gives you a spreadsheet (CSV) for your reimbursement form.

**Use it here:** https://ptrostli.github.io/mileage-log/

## How to use it

1. **Set your office.** You only do this once. Every trip starts and ends there.
2. **Add your trips.** Paste the week's addresses, one per line, or add them one at a time. A line can start with its date (`10/14`, `Oct 14`, or `Tuesday`).
3. **Check and save.** Make sure each place is the right one. If it isn't, pick another match or retype it.
4. **Download the spreadsheet.** Pick a month and click **Download for Excel**. You get a formatted .xlsx file with totals that opens in Excel, Numbers, or Google Sheets. **CSV** next to it gives a plain version.

Under **Settings and backup** you can:
- set a per-mile rate to get dollar amounts
- turn trip dates off
- download a backup of your trips

On a phone, use **Add to Home Screen** so it opens like an app.

## Where your data lives

Everything you enter is saved only in your own browser on your own device. Nothing is stored on GitHub or anywhere else. Download a backup now and then, because clearing your browser data erases your trips.

To find addresses and measure the drives, the app sends the address you type to two free OpenStreetMap services. They see the search, not your name or your saved trips.
- [Photon](https://photon.komoot.io) finds the addresses.
- [OSRM](https://project-osrm.org) works out the driving distance.

Distances follow the usual driving route between the two places. They aren't GPS tracking of the road you actually took. If you took a detour, use **Edit miles** to change the numbers.

## For development

- The whole app is one file: `index.html`. It has no build step and no dependencies.
- To run it locally, open `index.html` in a browser.
- Pushing to `main` redeploys the site on GitHub Pages within a minute or two.
- Open https://ptrostli.github.io/mileage-log/#test to get a **Reset app (testing)** button. Two taps wipes everything saved in that browser.
