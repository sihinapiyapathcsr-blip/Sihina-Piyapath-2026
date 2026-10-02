# Sihina Piyapath 2.0 — Website

CSR project website for the 03A Weekday Batch, SAB Campus of CA Sri Lanka.
Plain HTML/CSS/JS with no build step, so anyone on the team can edit it straight on GitHub.

## Folder layout

```
index.html          the whole page (text, sections, team names)
css/style.css       colours and layout
js/config.js        ⭐ settings you will edit: Google Sheet link, WhatsApp number, dates
js/main.js          live book list, WhatsApp buttons, countdown, photo viewer
images/             logo, school photos (school/), first project photos (sp1/)
videos/             first project videos + poster images
```

## 1. Put the site on GitHub Pages (one time)

1. Create a GitHub account, then click **New repository**. Name it `sihina-piyapath` and make it **Public**.
2. On the new repository page, click **uploading an existing file**. Drag **everything inside this folder**
   (index.html, README.md and the css, js, images and videos folders) into the box. Click **Commit changes**.
3. Go to **Settings → Pages**. Under *Branch*, choose **main** and **/ (root)**, then **Save**.
4. After 1–2 minutes your site is live at `https://YOUR-USERNAME.github.io/sihina-piyapath/`.

## 2. Connect the live book list (one time)

1. Open the Book Tracker in Google Sheets.
2. **File → Share → Publish to web**. In the first dropdown pick **Book List**. In the second pick
   **Comma-separated values (.csv)**. Click **Publish** and copy the link.
3. On GitHub, open `js/config.js`, click the ✏️ pencil, and paste the link between the quotes:
   `SHEET_CSV_URL: "https://docs.google.com/spreadsheets/d/e/....../pub?gid=...&single=true&output=csv",`
4. Click **Commit changes**. Done. From now on, just update **Received** in the Google Sheet and the
   website follows (Google can take about 5 minutes to refresh).

Until a link is pasted, the site shows the starting list (everything at 0).

## 3. Everyday edits

| To change… | Edit |
|---|---|
| Who gets "I'll donate this" messages | `WHATSAPP_NUMBER` in `js/config.js` |
| Drop-off deadline / donation day | `DROP_OFF_DEADLINE`, `DONATION_DAY` in `js/config.js`. Also update the text in `index.html` (search for "14 Oct" and "30 Oct"). |
| Text, team names, contact cards | `index.html` (search for the words you want to change) |
| A photo | Upload a new file with the **same name** into `images/…` to replace it |

Keep photos under about 300 KB each (resize to 1400 px wide) so the page loads fast on mobile data.

## 4. After the donation day (30 Oct)

Add a "2.0 Donation Day" gallery: copy the `<section ... id="story">` block in `index.html`,
change the text and point it at new photos in a new `images/sp2/` folder.

## Notes

- Dilshan's WhatsApp button uses his WhatsApp QR link (his number is never shown). If he taps
  "Reset QR code" in WhatsApp, that link stops working and must be replaced in `index.html`.
- Publish **only the Book List tab** of the Google Sheet.
