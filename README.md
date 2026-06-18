# Speed Reader

Fixation-point reading for the web and PDFs. Speed Reader bolds the first part of
each word so your eyes lock onto anchor points and glide through text faster with dyslexia-friendly font option.

## How it works (on-demand, privacy-first)

Speed Reader requests **no standing access to your browsing**. It runs on a page
only when you activate it there — by opening the popup and using the switch, or
by pressing **Alt+B**. At that moment it injects its formatter into that one tab
(via Chrome's `activeTab`) and reformats the text locally. The extension does not
send page text to the developer.

## Link to chrome extention



## PDF reader

**Online PDFs** — when you're viewing a PDF, open the popup and click "Open in
Speed Reader". Chrome asks for access to that one site only (never "all sites"),
then the PDF opens in the reader. Permission is granted per site, on demand.

**Local & Google Drive PDFs** — open the viewer (popup → "PDF reader") and drop a
file in, choose one from your computer, or paste a link. For Drive, download the
file then drop it in. No permission required, since you provide the file.

Either way the PDF is re-rendered as clean, reflowable text — page markers, heading
detection, de-hyphenation — with the same fixation controls. Powered by a bundled
copy of Mozilla's PDF.js. Remote PDFs are fetched directly by your browser from
their source; nothing is uploaded to the developer. Scanned/image-only PDFs are
detected and flagged (OCR is on the roadmap).

## What changed from the auto-everywhere model

Earlier builds injected on every page automatically (broad host permission). This
version uses on-demand activation instead, so the install shows **no "read all your
data on all sites" warning** and reviews faster. The trade-off: formatting starts
with one click/shortcut per page rather than automatically. A future optional
"auto-run on chosen sites" mode can be added via Chrome's optional permissions.

## Submission files

- `PRIVACY.md` — privacy policy (host it publicly and put the URL in the listing)
- `STORE_LISTING.md` — name, descriptions, permission justifications, asset specs


## "Use on all sites" (optional, opt-in)

By default Speed Reader runs only on the page you activate it on (activeTab — no
install warning). After a few uses, the popup proactively offers "Use Speed Reader
on all sites"; this offer can be dismissed, but the option stays permanently
available as a link at the bottom of the popup, so it's never a dead-end. Turning
it on requests broad host access once, then reading mode applies automatically
everywhere until turned off (which revokes access).

Per-site memory: whenever you grant Speed Reader access to a specific site (e.g.
by opening a PDF there, or enabling all-sites), the extension remembers it and
auto-activates on every page of that site on future visits — no need to toggle it
on again.


## Google Docs, Slides & Sheets

Google Docs renders text in a canvas, so it can't be formatted in place. Instead,
when you're on a Google Doc, Slide, or Sheet, the popup offers "Open in Speed
Reader": it opens that document's PDF export in the built-in reader (using your
own Google session, so it only works for docs you can already open).


## Tables, charts & complex layouts (View original page)

The reader extracts text and bitmap images for clean, reflowable reading — but
tables and vector charts (common in slide decks and scientific PDFs) don't survive
text extraction, since a PDF has no notion of a "table" and vector graphics aren't
images. For these, every page break has a **"View original page"** button that
renders the full page exactly as designed (tables, charts, vector graphics, layout)
as an image, on demand. You keep fast bionic reading for the prose and full visual
fidelity whenever you need it.

## Roadmap

OCR for scanned PDFs, reading stats, optional auto-run permission for trusted sites.
