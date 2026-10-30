# HBD-v3

A personalised birthday microsite for Anya, with animated headings and a sequence of sections leading to the birthday message. Open the top-level `index.html` to view the greeting and its digital-gift presentation.

## Preview locally

Open `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit http://localhost:8000. After changes, review the text, colours, images, and animation timing together. Preserve the relative locations of referenced media files; if media is missing, check that its path still matches its location. No deployment configuration is documented; serve the page and its media as static files with their relative paths intact.

## Personalizing the page

The page title is “Happy Birthday, Anya — from Ayush, by Pixel Studio”. When changing who the greeting is for or who it is from, review both the title and the visible message in `index.html` so they remain consistent. The document links to Fraunces and Manrope through Google Fonts; keep the font link and corresponding page styling in sync if you change typefaces.

Before moving or replacing media, check the references in `index.html`. Keep each file at its current relative location or update its reference to match the new location. Preview the text, colours, images, and animation timing together after edits.