# LinkedIn Job Filter

A clean, single-file HTML tool for building targeted LinkedIn job search URLs — with time filters, location, work model, job type, salary, experience level, and quick presets.

## Features

- **Full search form** — keyword, location, date posted, sort order, salary, experience level
- **Work model chips** — On-site, Remote, Hybrid
- **Job type chips** — Full-time, Part-time, Contract, Temporary, Volunteer, Internship
- **Quick Filters** — one-click presets for Past Hour, Past 6 Hours, Past 24 Hours, and Reset All
- **Live URL preview** — see the exact LinkedIn URL update as you change any filter, with one-click copy
- **Light / dark mode toggle**
- No logins. No tracking. No ads. No dependencies. Pure HTML/CSS/JS.

## Usage

### Option 1: GitHub Pages (recommended)
1. Upload `index.html` to your GitHub repo
2. Go to **Settings → Pages → Source: `main` branch, `/ (root)`**
3. Your tool is live at `https://yourusername.github.io/linkedin-job-filter/`

### Option 2: Open locally
Just open `index.html` in any browser. No server needed.

## Customization

**Change the default keyword** — open `index.html` and find:
```html
value="Quality Control Chemist"
```
Replace with your preferred default search term.

**Change the default time filter** — find the `<select id="sel-time">` block and move `selected` to your preferred option:
```html
<option value="r3600" selected>Past Hour</option>
```

## How the URL filter works

The `f_TPR=rN` parameter in the LinkedIn URL sets the time range in seconds:

| Value | Time range |
|-------|-----------|
| `r3600` | Past 1 hour |
| `r21600` | Past 6 hours |
| `r86400` | Past 24 hours |
| `r604800` | Past week |
| `r2592000` | Past month |

Other key parameters:
- `f_WT` — Work model (1=On-site, 2=Remote, 3=Hybrid)
- `f_JT` — Job type (F=Full-time, P=Part-time, C=Contract, T=Temporary, I=Internship)
- `f_E` — Experience level (1=Internship … 6=Executive)
- `f_SB2` — Minimum salary
- `sortBy` — R=Relevance, DD=Date posted

> **Note:** You must have a LinkedIn account and be signed in to view results.

---

Built for a biotech/pharma job search workflow.
