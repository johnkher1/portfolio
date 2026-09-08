# John Kher S. — Portfolio Site

Plain HTML/CSS/JS. No build step, no framework — open `index.html` in a
browser and it works as-is.

## Files

- `index.html` — all page content and structure
- `style.css` — all styling (colors, type, layout are defined as CSS
  variables at the top of the file under `:root`)
- `script.js` — mobile menu toggle, footer year, and the scroll-progress
  rail on the left edge of the page

## Things to personalize before sending this to clients

Search for these in `index.html` and swap in your real info:

- `your.email@example.com` — your real email (appears once in the Contact section)
- `github.com/your-username` and the matching `href="https://github.com/your-username"`
- The Upwork link is already set to your profile URL — double check it's correct
- **Card 1 (Scholarship Management System)** already links to
  `https://kabscholarsystem.website/login` and opens in a new tab
- **Card 2 (FastAPI Task Tracker)** is still a placeholder project —
  replace with real client work as you get it, or delete the card
- **Card 3 (Video Editing Samples)** links to the new `#video-samples`
  section further down the page — see below
- The project "thumb" blocks are plain CSS patterns, not images. If you'd
  rather use screenshots, replace the `<div class="project-thumb">` with an
  `<img>` tag

## Video samples

The **Video samples** section (`id="video-samples"`) now plays your four
real clips directly from `assets/`:

```
assets/
├── clip-01.mp4
├── clip-02.mp4
├── clip-03.mp4
└── clip-04.mp4
```

Each one is a plain HTML5 `<video controls>` element — no YouTube, no
Vimeo, nothing external. To add a fifth clip later, copy one `<video>`
block in `index.html`, point its `<source>` at a new file
(e.g. `assets/clip-05.mp4`), and drop that file into `assets/`. The grid
wraps automatically, so there's no fixed limit.

A couple of notes on hosting video files specifically:

- **GitHub Pages** serves these fine, but GitHub warns/limits individual
  files over 100MB and repos over ~1GB — your current four clips
  (~23MB total) are well within that.
- If your clips grow much larger or more numerous later, consider
  compressing them (e.g. with HandBrake) before adding, since large video
  files slow down page load for site visitors on mobile data.

## Colors & fonts

Open `style.css` and edit the `:root` block at the top — every color and
both fonts are defined there once, so changing `--accent` (currently a
warm amber) updates every button, link-hover, and highlight across the
whole site.

## Publishing

See the deployment steps in the chat where this was generated. Short
version: this is a static site, so GitHub Pages or Netlify both work with
zero configuration — just upload these three files (`index.html`,
`style.css`, `script.js`).
