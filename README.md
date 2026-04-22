# LinkedIn Job Filter

A lightweight, single-file HTML tool for quick access to LinkedIn job search links filtered by how recently they were posted.

## Features

- 6 time filters: 1 hour, 2 hours, 3 hours, 6 hours, 24 hours, 3 days
- Live keyword editor — change the search term, links update instantly
- One-click copy URL button per filter
- One-click open on LinkedIn per filter
- "Open All" button to launch all 6 filters at once
- Light / dark mode toggle
- No dependencies, no build step — pure HTML/CSS/JS

## Usage

### Option 1: GitHub Pages (recommended)
1. Fork or upload this repo to GitHub
2. Go to Settings → Pages → Source: `main` branch, `/ (root)`
3. Your tool is live at `https://yourusername.github.io/linkedin-job-filter/`

### Option 2: Open locally
Just open `index.html` in any browser. No server needed.

## Customization

To change the default keyword, open `index.html` and find:
```html
value="Quality Control Chemist"
```
Replace with your preferred default search term.

To add or remove time filters, edit the `FILTERS` array in the `<script>` section:
```js
const FILTERS = [
  { label: "Last 1 Hour",  seconds: 3600   },
  { label: "Last 2 Hours", seconds: 7200   },
  ...
];
```

## How the URL filter works

The `f_TPR=rN` parameter in the LinkedIn URL sets the time range in seconds:
- `r3600` = last 1 hour
- `r86400` = last 24 hours
- `r259200` = last 3 days

---

Built for a biotech/pharma job search workflow.
