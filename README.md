# HBD-v3

HBD-v3 is a birthday tribute for Anya from Ayush, with animated headings, photos, a cupcake interaction, balloons, and a final wish. The page is hard-coded for this greeting: it has no URL-based personalization controls. Its top-level `index.html` is the entry point, and the visible names and document title should both be reviewed when adapting it.

## Preview locally

Open `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000). Fraunces and Manrope are loaded from Google Fonts, so those typefaces require network access. The favicon is an inline SVG.

## Page interactions

The hero heading cycles through four messages every 4.2 seconds using a character-scramble effect. Other marked headings scramble on hover, and marked labels scramble as they are revealed while scrolling. The page also includes a scrolling text ticker and scroll-triggered reveal effects.

Tap the cupcake once to light its candle and tap again to blow it out and change the wish message. There is no relight control. Three balloons reveal separate wishes when tapped; a counter tracks the releases, and the third balloon triggers a final wish. There is no balloon reset control. The cupcake and balloon state is held in JavaScript and resets on page reload.

## Photos, motion, and editing

The two photo slots load `images/anya-1.jpg` and `images/anya-2.jpg`. If either image fails to load, the page displays an inline SVG “PHOTO ON ITS WAY” illustration. Keep these relative paths intact when publishing, or update the image references in `index.html` when replacing or moving the files.

The page requests Fraunces and Manrope from Google Fonts. Edit the hard-coded greeting, title, sections, styles, and interactions in `index.html`; there is no URL personalization or application API call, and the page does not use local or session storage. The CSS reduced-motion mode disables CSS animations and transitions, but the JavaScript heading-scramble interval is not conditioned on the reduced-motion preference, so that text effect continues. Review names, personal details, and photos before sharing. For static hosting, include the entry page and its referenced images with their relative paths preserved.