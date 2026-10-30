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

## Configuration and data handling

This repository is a static page with no environment template or backend configuration listed. Never place credentials or private values in tracked HTML or assets: browser-delivered content is visible to visitors and cannot be secret. The greeting identifies people, so review names, personal details, and media before sharing or publishing the page. Linked Google Fonts are served from an external service and may be requested by visitors' browsers.

## Browser and layout review checklist

This is a checklist for future review, not a report of completed compatibility testing or verified results.

- Open `index.html` in current versions of browsers relevant to the page's intended audience. Also load it through the local server above to review relative paths in a served-page context.
- Read the greeting and scroll through the sections to the birthday message. Observe animated headings after related edits.
- Inspect the browser console during load and while moving through the page. Investigate errors that could affect the sections, message, or animation.
- Inspect the Network panel for failed requests. Check each local media reference in `index.html` against its file path and confirm the media appears. Check requests for Fraunces and Manrope from Google Fonts, and confirm those remote requests are intentional; consider the page's typography if the fonts cannot load.
- Inspect the page at a narrow phone-sized viewport and a wide desktop-sized viewport. Check text, colors, images, and section layout for clipping or overflow.
- Review media dimensions and file sizes for their intended display. Before removing assets, check that no page or style still uses them; update references when moving files.

## Accessibility review checklist

Use these as future review steps; they are not verified results.

- Move through the greeting and sections using only a keyboard. Check that any links or controls can be focused and operated without pointer input.
- Check keyboard focus visibility against the page's backgrounds and through the sequence of sections.
- Review links and controls for meaningful names. Check that the birthday message and digital-gift presentation are understandable without relying only on visual styling or animation.
- Check text contrast throughout the page, including text placed over images or decorative areas.
- Check referenced images for appropriate text alternatives when they convey meaningful content; avoid redundant alternatives for decorative images.
- Check animated headings and other motion with reduced motion requested, and consider reducing or stopping nonessential animation.