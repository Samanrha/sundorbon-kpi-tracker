# Sundorbon KPI Tracker

Multi-site weekly operations dashboard for M95 Kitchens Group
(Sundorbon Bridport, Sundorbon Dorchester, Rivaaz Lymington).

Static single-page app — no build step, no server. Deploys to Netlify
as a plain static publish.

## Features
- **Weekly Tracker** — delivery-platform figures (Just Eat, Uber Eats,
  Deliveroo): orders, sales, ratings, reviews, promo spend/revenue,
  commission → live AOV, ROAS, net. Plus an EOD trading summary.
- **Revenue** — daily (Mon–Sun) revenue grid totalling to weekly.
  Bridport & Rivaaz = Orderlord + Tevalis; Dorchester = Orderlord only.
  Orderlord auto-fills per day from the EOD app.
- **KPI Dashboard** — full MSA KPI scorecard (clause 5 / Schedule M-1)
  with editable targets and RAG status, clause 11.3 bonus eligibility,
  and a one-click weekly report for Mash.

## Data & integration
- Data is stored per browser via `localStorage` (per-origin).
- Orderlord turnover is pulled from the M95 EOD Google Apps Script web
  app via JSONP (`getWeekSummary` action).

## Deploy (Netlify)
Static publish of the repo root. No environment variables required.
