# Home Energy Data

Client-side tools for exploring home energy consumption and comparing electricity tariffs.

## Tariff cost calculator

Open `index.html` (or the deployed GitHub Pages site) and upload a PTU CSV
(`period_start_local`, `period_end_local`, `energy_kwh`, or an Octopus export with
`Start`, `End`, `Consumption (kwh)`). Configure tariff bands and
compare annual/monthly costs. All processing happens in the browser; no data leaves
your machine.

Sample data files are included in the repository root:
- `grid_consumption_hourly_12m.csv`
- `grid_consumption_30min_recent.csv`

## GitHub Pages

This repository is a static site and is compatible with GitHub Pages.

- `.nojekyll` disables Jekyll processing so all files (including CSV data) are
  served as-is.
- `index.html` is the entry point.
- `tariffs.json` holds the built-in tariff set; edit it (and bump nothing —
  redeploy) to update tariffs for all users. User-created tariffs are stored
  locally in the browser.
- `sw.js` is a service worker providing offline support and background updates
  of `tariffs.json`.
- Deployment: GitHub Pages serves from the `main` branch (root). In repo
  settings set Pages source to "Deploy from a branch" (main, /). No Actions
  workflow is required.

To enable: in the repository settings, set Pages source to "GitHub Actions".