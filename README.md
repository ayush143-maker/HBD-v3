# HBD-v3

A personalised birthday microsite for Anya, with animated headings and a sequence of sections leading to the birthday message. Open the top-level `index.html` to view the greeting and its digital-gift presentation.

## Preview locally

Open `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit http://localhost:8000. No deployment configuration is documented; serve the page and its media as static files with their relative paths intact.

## Personalizing the page

The page title is “Happy Birthday, Anya — from Ayush, by Pixel Studio”. When changing who the greeting is for or who it is from, review both the title and the visible message in `index.html` so they remain consistent. The document links to Fraunces and Manrope through Google Fonts; keep the font link and corresponding page styling in sync if you change typefaces.

Before moving or replacing media, check the references in `index.html`. Keep each file at its current relative location or update its reference to match the new location.

## Manual review checklist

Use these actions as a review guide; they are not verified results or measured performance.

- Open `index.html` in a browser, or visit `http://localhost:8000` after starting the local server above.
- Read the greeting and scroll through the sections to the birthday message. Observe the animated headings after related edits.
- Check each local image, audio, and font path referenced in `index.html` against an existing file, then review the page for missing media.
- Review media dimensions and file sizes for their intended display. Avoid oversized files, and remove assets only after checking that no page or style still uses them.
- The page links to Fraunces and Manrope through Google Fonts. Confirm that this external font dependency is intentional and that the linked families are used; keep the font link and styling in sync when changing typefaces. Check any external script references before adding or retaining them.
- Inspect the page at a narrow phone-sized viewport and a wide desktop-sized viewport. Check the text, colours, images, and section layout.

## Accessibility review checklist

Use these as future review steps; they are not verified results.

- Move through the greeting and sections using only a keyboard. Check that any links or controls can be focused and operated without pointer input.
- Check keyboard focus visibility against the page's backgrounds and through the sequence of sections.
- Review links and controls for meaningful names. Check that the birthday message and digital-gift presentation are understandable without relying only on visual styling or animation.
- Check text contrast throughout the page, including text placed over images or decorative areas.
- Check referenced images for appropriate text alternatives when they convey meaningful content; avoid redundant alternatives for decorative images.
- Check animated headings and other motion with reduced motion requested, and consider reducing or stopping nonessential animation.