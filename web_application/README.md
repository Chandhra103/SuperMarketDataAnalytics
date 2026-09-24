# Super Market Data Analytics — Web Application

This is the React + Vite dashboard for the Super Market Data Analytics internship project.

## Features

- Executive overview with real supermarket KPIs
- Sales and product/category analysis
- Customer type analysis
- Branch and city comparison
- Payment-method analysis
- Rating distribution and category rating analysis
- Fact → Insight → Opportunity/Risk → Action business recommendations
- City, branch, category, and customer-type filters
- Responsive teal, dark navy, and light neutral analytics theme

## Dataset integration

The dashboard uses the validated 500-row supermarket dataset. The generated `src/data.ts` module contains the same records as the repository-level `dataset/supermarket_data.csv` so the static frontend can run without a backend or demo data source.

## Run locally

```bash
pnpm install
pnpm dev
```

For a production build:

```bash
pnpm check
pnpm build
```

The project uses React, TypeScript, Vite, Recharts, and Lucide icons. No backend, database, or generic e-commerce data is required.
