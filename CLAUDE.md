# CLAUDE.md

Personal academic website of **Hriday Ranka** — CS Master's student at NYU Courant ('27).
Hosted at `https://cs.nyu.edu/~hsr3649/`. This is a plain, hand-written static site:
no build step, no framework, no JS dependencies. Just HTML files with inline `<style>`.

## How to work on this site

- Every page is a **single self-contained `.html` file** with its CSS in a `<style>` block
  in the `<head>`. There is no shared stylesheet — each page repeats the base styles.
  When editing styles, keep the per-page copies consistent rather than introducing a
  shared file (unless explicitly asked to refactor).
- No tooling. To preview, just open the file in a browser (or `python3 -m http.server`).
- Deployment is by copying files to the NYU Courant web host; there is no CI/pipeline.

## Taste & aesthetic (keep this consistent)

The whole site is deliberately **minimal, text-first, and academic**. Treat this as the
guiding style for any new page or edit:

- **Typography:** body text is `'Times New Roman', Times, serif`. The homepage name/headings
  use the `Merriweather` serif from Google Fonts. Stick to serif; avoid sans-serif and
  decorative fonts. (The retired `og.html` used `Courier New` monospace — that era is over.)
- **Palette:** strictly black on white. `--bg:#fff; --fg:#000; --muted:#444`. The ONLY
  accent is `color: blue` for inline content links. Don't add new colors.
- **Layout:** centered single column, `max-width` ~800px on content pages (1040px on the
  homepage). Generous padding (`48px 16px`), justified body paragraphs (`text-align: justify`),
  `line-height: 1.6`, body font-size `18px`.
- **Voice:** the writing is lowercase, personal, understated, and honest — e.g. "right now
  im just trying to find where i belong", and `<s>strikethrough</s>` used to show abandoned
  interests. Preserve this lowercase, candid tone. Don't "professionalize" or over-polish copy
  unless asked. Headings/titles may use Title Case; prose stays lowercase.
- Content pages all open with a `← back to home` link (class `back-link`) to `index.html`.
- Mobile matters: keep the responsive `@media` breakpoints working (homepage stacks its
  two-column grid at 700px).

## Pages

- `index.html` — homepage. Banner image + italic quote, name/social icons header, a short
  "brief introduction" bio with links out to the topic pages, profile photo, `[CV]` link.
- `algorithms.html` — personal dedication page about Honors Analysis of Algorithms / Prof.
  Subhash Khot. Photos with italic captions.
- `complexity.html` — running notes index for the Complexity course (links to Google Drive PDFs).
- `reinforcement_learning.html` — lecture-by-lecture notes index for David Silver's RL course
  (links to Google Drive PDFs / YouTube).
- `omarchy.html` — fullscreen photo of the current Omarchy (Linux) desktop setup.
- `og.html` — archived previous version of the site ("what this site used to be"), monospace style.
- `google297e8aa129dfa7e3.html` — Google Search Console verification file. Don't touch/delete.

## Assets

- Images: `banner.webp`, `new.jpg` (profile), `teaching.jpeg`, `walking.jpeg`, `studybuddy*.jpeg`,
  `omarchy.jpg`. `favicon.png` is the site icon.
- `cv.pdf` — linked CV.
- Some images are large (multi-MB); prefer `.webp` and reasonable sizing for any new images.

## Conventions

- Inline content links that point to topic pages or external resources use `style="color: blue"`.
- New lecture/notes entries follow the existing list patterns (`.lecture-list` /
  ordered list) and link to Drive/YouTube.
- Keep `<meta name="description">`, `<title>`, and the `canonical` link on `index.html` accurate
  when the bio changes.
