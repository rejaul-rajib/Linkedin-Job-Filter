# LinkedIn Job Filter

A single-file HTML tool for building targeted LinkedIn job search URLs — no login, no tracking, no dependencies.

## Features

- **Search form** — keyword, location, date posted, sort order, salary, experience level
- **Work model** — On-site, Remote, Hybrid
- **Job type** — Full-time, Part-time, Contract, Temporary, Volunteer, Internship
- **Quick Filters** — Past Hour, Past 6 Hours, Past 24 Hours, Reset All
- **Live URL preview** — updates as you type, with one-click copy
- **Light / dark mode toggle**

## Deploy

### GitHub Pages
1. Upload `index.html` to your repo
2. Go to **Settings → Pages → Source: `main` branch, `/ (root)`**
3. Live at `https://yourusername.github.io/linkedin-job-filter/`

### Local
Open `index.html` in any browser. No server needed.

## Customization

**Default time filter** — find `<select id="sel-time">` and move `selected` to your preferred option:
```html
<option value="r3600" selected>Past Hour</option>
```

## How the URL filter works

`f_TPR=rN` sets the time range in seconds:

| Value | Range |
|-------|-------|
| `r3600` | Past 1 hour |
| `r21600` | Past 6 hours |
| `r86400` | Past 24 hours |
| `r604800` | Past week |
| `r2592000` | Past month |

Other parameters:
- `f_WT` — Work model (1=On-site, 2=Remote, 3=Hybrid)
- `f_JT` — Job type (F=Full-time, P=Part-time, C=Contract, T=Temporary, I=Internship)
- `f_E` — Experience level (1=Internship … 6=Executive)
- `f_SB2` — Minimum salary
- `sortBy` — R=Relevance, DD=Date posted

> You must have a LinkedIn account and be signed in to view results.

---

Built for a biotech/pharma job search workflow.
