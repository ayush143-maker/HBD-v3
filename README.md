# HBD-v3

HBD-v3 is a personalised birthday microsite for Anya, with animated headings and a sequence of sections leading to the birthday message. The top-level `index.html` is the page entry point; its title is “Happy Birthday, Anya — from Ayush, by Pixel Studio”.

## Preview locally

Open `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000). The page requests Fraunces and Manrope from Google Fonts, which require network access to that service.

## Personalize the page

When changing who the greeting is for or from, review both the document title and visible message in `index.html`. If changing typefaces, keep the Google Fonts links and corresponding styling in sync. Before moving or replacing media, check its references in `index.html`; preserve each relative path or update the reference to match the new location.

Review names, personal details, and media before sharing or publishing. Visitors can inspect files delivered to their browser, so do not put credentials or secrets in the page.

## Repository map

- `index.html` — page entry point, greeting, sections, and resource references.

No build step, generated output directory, or deployment configuration is documented. For a static publication, include the top-level page and the files it references. After editing, preview the page at narrow and wide viewport sizes, scroll through the sections to the birthday message, and check the animated headings and media in context. Consider the appearance when external fonts cannot load.