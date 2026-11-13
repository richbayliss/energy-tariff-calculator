# Home Energy Data

Client-side tools for exploring home energy consumption and comparing electricity tariffs.

## Tariff cost calculator

Open `index.html` (or the deployed GitHub Pages site) and upload an hourly PTU CSV
(`period_start_local`, `period_end_local`, `energy_kwh`). Configure tariff bands and
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
- Deployment is automated via `.github/workflows/deploy-pages.yml`.

To enable: in the repository settings, set Pages source to "GitHub Actions".