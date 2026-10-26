# Njoki Mwihaki — Personal Site

## Files

```
NjokiM-NjokiM.github.io/
├── index.html                  ← Homepage / blog index
├── about.html                  ← About page
├── resume.html                 ← Résumé (software, data, AI, geospatial)
├── contact.html                ← Contact page
├── Maureen_Njoki_Resume.pdf    ← Print/email version of the résumé (3 pages, A4)
├── assets/
│   ├── css/
│   │   ├── style.css           ← Site styles (shared tokens)
│   │   └── resume.css          ← Résumé styles + print stylesheet
│   ├── img/njoki-headshot.jpg  ← Header portrait (600×600, cropped from NJOKI_2025.JPG)
│   └── js/main.js              ← Mobile nav
└── README.md
```

## Content notes

The site is a general portfolio: it is not tailored to any single client or
tender. It advertises WordPress and Django website builds plus data
engineering work, and the résumé carries a plain-language
"Past work & technical projects" summary for non-technical readers.

When editing that summary, keep it in the full-width `.case-list` layout.
Chrome emits per-glyph positioning inside the narrow `.spec` cards, which
makes PDF text extraction collapse spaces (`Why it matters` becomes
`Whyitmatters`). Full-width lists keep the text layer clean and stay
readable for non-technical readers.

## Live

- Site: https://njokim.github.io/NjokiM-NjokiM.github.io/
- Résumé: https://njokim.github.io/NjokiM-NjokiM.github.io/resume.html

## Regenerating the PDF

`resume.css` carries a `@media print` block that turns the page white and
A4-sized. To rebuild the PDF, serve the folder and print through Chrome's
DevTools protocol (`Page.printToPDF` with `printBackground: true` and
`preferCSSPageSize: true`).

Note: Chrome's `--print-to-pdf` command-line flag hangs on macOS with this
page; use the CDP route instead.
