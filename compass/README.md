# Marketing Analytics Dashboard 📊

An interactive **marketing / e-commerce analytics dashboard** built with **Plotly** —
a reconstruction of a data-analytics project (originally done at **a cloud-consulting firm**), redesigned
to run **end-to-end locally** and deploy as a free **GitHub Pages** demo (no cloud bill).

👉 **Live demo:** open `index.html` (a self-contained page — Plotly loads from CDN).

## What it shows
A single-page dashboard over one year of (synthetic, plausible) marketing data across
**6 channels** and **5 regions**:
- **KPI cards** — Revenue, Ad Spend, **ROAS**, Conversion Rate, Avg Order Value, **CAC**.
- **Revenue over time** — daily bars + 7-day moving average (weekly + year-end seasonality).
- **Revenue by channel** — horizontal bars annotated with ROAS per channel.
- **Conversion funnel** — Impressions → Clicks → Conversions with drop-off %.
- **Revenue treemap** — by region and channel.

## How it works
`build_dashboard.py`:
1. **Generates** a plausible dataset (`data/marketing.csv`) with realistic CTR/CVR/CPC per
   channel + seasonality (deterministic seed).
2. **Computes** the KPIs (ROAS, CVR, AOV, CAC).
3. **Renders** four Plotly figures and writes a styled, self-contained `index.html`.

## Run
```bash
pip install -r requirements.txt
python build_dashboard.py      # regenerates data/ + index.html
```

## Notes
- **Synthetic data** (no client data) — the original project's data isn't published.
- Static page → hostable on **GitHub Pages / github.io** as-is (just serve `index.html`).
- Stack: `plotly`, `pandas`, `numpy`.

> Data Science / data-viz portfolio piece. Demonstrates the analytics pipeline (collect → KPI → interactive viz) as a hostable demo.
