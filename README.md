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
