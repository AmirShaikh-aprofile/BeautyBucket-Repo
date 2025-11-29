# BeautyBucket (Google Sheets + GitHub Pages)

This project implements a lightweight cosmetics storefront using Google Sheets as the admin/data backend and GitHub Pages for free hosting.

## What you received
- `index.html` — client website (static). Edit PRODUCTS_CSV_URL inside the script to point to your published Google Sheet CSV.
- `admin.html` — admin instructions and template download link.
- `templates/` — CSV templates for products and dealer quotations.
- `styles.css` — styling for both pages.
- `images/` — put placeholder images here if you want to host images on GitHub Pages.

## How to setup Google Sheet
1. Create a new Google Sheet.
2. Use File → Import → upload `products_template.csv`.
3. (Optional) Create a second sheet / tab for `Dealers` and import `dealers_template.csv`.
4. File → Publish to web → choose the products sheet and `Comma separated values (CSV)` → Publish → copy the generated link.
5. Use the CSV link in `index.html`:
   Replace `REPLACE_WITH_PRODUCTS_CSV_URL` with:
   `https://docs.google.com/spreadsheets/d/YOUR_SHEET_ID/export?format=csv&gid=0`

## GitHub Pages deployment
1. Create a new public GitHub repo (e.g., `BeautyBucket-site`).
2. Upload the contents of the `frontend/` folder to the repo root (index.html, styles.css, templates/, images/).
3. In repository Settings → Pages, set source to `main` branch and directory `/` (root). Save.
4. Visit the generated GitHub Pages URL.

## QR Code
Once site is live on GitHub Pages, generate a QR code pointing to the Pages URL with any free QR generator.

## Notes
- Google Sheets caching may delay updates by ~1 minute.
- For product images: use public URLs in the sheet, or upload images to your GitHub repo `images/` folder and reference `https://your-username.github.io/your-repo/images/imagename.jpg`.
- If you want the dealer quotes to be editable from an admin web UI later, we can add a simple admin page that writes via the Google Sheets API — that requires a bit more setup (Google Cloud credentials).
