# Laundry Guide

A personal laundry system for a **new washer**: powder-only cleaning, enzyme booster for gym wear, citric acid instead of fabric softener — and why.

## Read the guide

- **Live site (GitHub Pages):** https://rcfilter.github.io/laundry/
- **Local file:** [`docs/index.html`](docs/index.html)
- **Markdown:** [`docs/guide.md`](docs/guide.md)
- **PDF:** open the live site or HTML → Print → Save as PDF

Pages deploys automatically from the `docs/` folder on every push to `main`.

### One-time setup (required)

GitHub Pages must be turned on once in the repo settings:

1. Open **Settings → Pages** for this repo  
2. Under **Build and deployment**, set **Source** to **GitHub Actions**  
3. Save — the [Deploy GitHub Pages](https://github.com/RCfilter/laundry/actions/workflows/pages.yml) workflow will run on the next push to `main` (or re-run the last failed run)

After that, the site is live at **https://rcfilter.github.io/laundry/**

## The stack

| Product | Role |
|---|---|
| 365 Unscented Powder | Main detergent |
| Dirty Labs Bio Enzyme Booster | Lipase / gym & body oils |
| Food-grade citric acid (dissolved) | Rinse aid in softener drawer |

**Avoid:** liquid detergent in the machine, fabric softener.

## Lipase list

[Community lipase detergent spreadsheet](https://docs.google.com/spreadsheets/d/1oHWzZ1Sth0Y0J2ynmXFl7M4mGZe-T_MJ_m_Y39pfBug/edit)

## Preview locally

```bash
python3 -m http.server 8080 --directory docs
```

http://localhost:8080
