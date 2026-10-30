# HBD-v3

A personalised birthday microsite for Anya, with animated headings and a sequence of sections leading to the birthday message. Open the top-level `index.html` to view the greeting and its digital-gift presentation.

## Preview locally

Open `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit http://localhost:8000. After changes, review the text, colours, images, and animation timing together. Preserve the relative locations of referenced media files; if media is missing, check that its path still matches its location. No deployment configuration is documented; serve the page and its media as static files with their relative paths intact.