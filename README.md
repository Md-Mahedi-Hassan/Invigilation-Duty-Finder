# Invigilation Duty Finder

A static GitHub Pages website that reads three repository PDFs in the browser:

- `duty-roster.pdf` - faculty duties, dates, slots, and examination notices
- `faculty-list.pdf` - designation, phone number, and email address
- `exam-committee.pdf` - committee role and contact information

## Upload to GitHub

Upload every file from this package directly to the repository root. There are
no required folders.

```text
.nojekyll
index.html
guidelines.html
committee.html
styles.css
app.js
guidelines.js
committee.js
theme.js
duty-roster.pdf
faculty-list.pdf
exam-committee.pdf
pdf.min.js
pdf.worker.js
pdf-lib.min.js
PDF.js-LICENSE.txt
```

Configure GitHub Pages:

```text
Settings > Pages
Source: Deploy from a branch
Branch: main
Folder: / (root)
```

## Update published information

Replace any PDF while keeping its exact repository filename:

```text
duty-roster.pdf
faculty-list.pdf
exam-committee.pdf
```

The website uses cache-busting requests, so refreshed pages read the newly
published PDFs. The replacement PDFs should preserve the same general table
structure and remain text-based rather than scanned images.

The committee PDF may include a column labeled `Room` or `Room No.`. Committee
portraits should be uploaded to the repository root as JPEG files named with
the exact faculty initial:

```text
AAK.jpeg
MJZ.jpeg
MHS.jpeg
```

If an image is missing, the website displays the member's initial instead.

When installing this version, replace all HTML, CSS, and JavaScript files in
the repository. The pages use Version 7 cache-busting query parameters so the
new layout is loaded instead of a previously cached copy.

Version 7 generates the individual roster PNG and PDF from the same canvas
design. The PDF is downloaded as one custom-sized page, so it is not split by
the browser's print pagination. The light/dark preference is stored only in
the visitor's browser.

Version 7 also reads the Exam Slot Schedule directly from `duty-roster.pdf` on
the Examination Guidelines page. If Slot A/B/C times are changed in the PDF,
the page displays the updated times after GitHub Pages redeploys and the browser
is hard-refreshed.

No server, database, PHP, XAMPP, or build command is required.
