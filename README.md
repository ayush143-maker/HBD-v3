# HBD-v3

A personalised birthday microsite for Anya, with animated headings and a sequence of sections leading to the birthday message. The top-level `index.html` is the page entry point. Its title is “Happy Birthday, Anya — from Ayush, by Pixel Studio”.

## Preview locally

Open the top-level `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit `http://localhost:8000`. The page requests Fraunces and Manrope from Google Fonts; those external fonts require network access to that service.

## Personalizing the page

- When changing who the greeting is for or who it is from, review both the document title and visible message in `index.html` so they remain consistent.
- The document links to Fraunces and Manrope through Google Fonts. If you change typefaces, keep the font link and corresponding page styling in sync.
- Before moving or replacing media, check its references in `index.html`. Keep each file at its referenced relative location or update the reference to match the new location.

## Deployment-readiness checklist

The supplied project information identifies a top-level `index.html` and does not document a build step, generated output directory, or deployment configuration. The items below are recommendations to verify for the publishing method you choose; they are not claims that publishing has been configured or completed.

### Before publishing

- [ ] **Choose and verify the document root.** For a static publication of this page, the selected root or output directory should contain `index.html` at its top level. If your publishing workflow requires a separate output directory, verify that the page and all files it references are included there. Do not assume an undocumented build step creates that directory.
- [ ] **Preserve relative asset paths.** Check every local file reference in `index.html`. Keep referenced files in their expected relative locations in the published files, or update the references to match their new locations. Check path spelling and capitalization.
- [ ] **Check external resources.** Confirm that the Google Fonts links are intentional and consider how the page will look if those requests cannot be loaded. Do not mistake an unavailable external font for a missing local file.
- [ ] **Review configuration and content for safety.** No environment template or backend configuration is listed. Do not put credentials, private values, or secrets in HTML or other browser-delivered files; visitors can inspect those files. Review names, personal details, and media before sharing or publishing the greeting.
- [ ] **Keep the published files focused.** Include the entry page and the assets it references. Do not rely on files outside the selected published directory unless the page is intentionally configured to load them from an external location.

### After publishing

- [ ] Open the published page at its resulting URL and confirm that the birthday greeting and sections appear as expected. This is a recommended final review, not a report that the page has been published or checked.
- [ ] Review the page in a browser at a narrow phone-sized viewport and a wide desktop-sized viewport. Check text, colors, images, and section layout for clipping or overflow.
- [ ] Check the browser console and Network panel for failed requests. Verify local asset paths separately from Google Fonts requests.
- [ ] Scroll through the page to the birthday message and observe the animated headings. Review any changed content and media in context.
- [ ] If something is missing or incorrect, check that the published root contains `index.html`, that local files were included at the expected relative paths, and that references in `index.html` match those paths.

## Troubleshooting

These are diagnostic steps, not claims that the page currently has a problem.

1. **Confirm the entry page and served directory.** Open the top-level `index.html`, or serve the repository directory and visit its root URL. If the greeting or sections do not appear as expected, confirm that the served directory is this project.
2. **Check local paths.** If media is missing, check that the referenced file exists at the path used by `index.html`. Preserve its relative location or update the reference when moving it.
3. **Inspect browser diagnostics.** Check the console during load and while moving through the page. Use the Network panel to inspect failed requests and URLs.
4. **Distinguish external fonts from local files.** Fraunces and Manrope are requested from Google Fonts and depend on network access to that service. Check font requests separately from local media, and consider the page's appearance if the fonts cannot load.

## Contributor handoff

Keep edits focused on the requested greeting, presentation, or related assets. Preserve existing filenames and relative references, or update the references in `index.html` when a file must move. In the handoff, briefly describe the files and content changed. Manually open the page and review affected sections and media before publishing; this is a recommended review step, not a claim that it has already been completed.

## Browser and accessibility review

The following are recommendations for review, not verified compatibility or accessibility results.

- Review the page in current versions of browsers relevant to its intended audience.
- Use only a keyboard to move through the greeting and sections. Check that links or controls can be focused and operated without pointer input, and that focus remains visible.
- Review links and controls for meaningful names. Check that the birthday message and digital-gift presentation are understandable without relying only on visual styling or animation.
- Check text contrast throughout the page, including text placed over images or decorative areas.
- Check referenced images for appropriate text alternatives when they convey meaningful content; avoid redundant alternatives for decorative images.
- Check animated headings and other motion with reduced motion requested, and consider reducing or stopping nonessential animation.

## Final release review

- Open `index.html` from the published location and confirm the page loads as expected.
- Test with network access available and keep a sensible fallback for externally loaded resources.
- Review the published result once on a narrow screen and once on a wider screen; treat this as a release check, not an automated test report.
