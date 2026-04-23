# LinkedIn Job Filter

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)
[![Live Demo](https://img.shields.io/badge/live%20demo-GitHub%20Pages-2ea44f.svg)](https://rejaul-rajib.github.io/linkedin-job-filter/)

A single-file HTML tool for building targeted LinkedIn job search URLs — no login, no tracking, no dependencies.

## Features

- Search form: keyword, location, date posted, sort order, salary, experience level.
- Work model: On-site, Remote, Hybrid.
- Job type: Full-time, Part-time, Contract, Temporary, Volunteer, Internship.
- Quick filters: Past Hour, Past 6 Hours, Past 24 Hours, Reset All.
- Live URL preview with one-click copy.
- Light / dark mode toggle.

## Deploy

### GitHub Pages
1. Upload `index.html` to your repo.
2. Go to **Settings → Pages**.
3. Set **Source** to `main` branch and `/ (root)`.
4. Open the live site at `https://rejaul-rajib.github.io/Linkedin-Job-Filter/`.

### Local
Open `index.html` in any browser. No server needed.

## Customize

To change the default date filter, find `<select id="sel-time">` and move `selected` to the option you want:

```html
<option value="r3600" selected>Past Hour</option>
```

## URL parameters

`f_TPR=rN` sets the time range in seconds.

| Value | Range |
|---|---|
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

## Bug reports

If you find a bug, please report it here:

[Report a bug](https://github.com/rejaul-rajib/linkedin-job-filter/issues/new)

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

Built by Rejaul Islam for biotech/pharma job searches.
