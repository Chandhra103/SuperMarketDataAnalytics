# SuperMarket Data Analytics — Web Application

This is the React + Vite dashboard for the SuperMarket Data Analytics internship project.

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

## Vercel Deployment

This is a Vite/React static frontend. The repository includes `vercel.json` with the required SPA fallback and output settings.

1. Push the project to GitHub.
2. Open [Vercel](https://vercel.com/) and choose **Add New Project**.
3. Import the existing `Chandhra103/SuperMarketDataAnalytics` repository.
4. Set the **Root Directory** to `web_application`.
5. Confirm the following project settings:
   - **Framework Preset:** Vite
   - **Install Command:** `pnpm install --frozen-lockfile`
   - **Build Command:** `pnpm build:vercel`
   - **Output Directory:** `dist/public`
6. Do not add environment variables. This static dashboard uses the validated dataset embedded in `src/data.ts` and does not require API keys or secrets.
7. Click **Deploy** and open the generated Vercel URL.

The `vercel.json` rewrite sends client-side paths to `index.html`, so the application remains accessible after refresh or direct navigation. The Vercel build runs only the Vite frontend build; the optional local Express server is not required for deployment.

## Folder structure

```text
web_application/
├── README.md
├── package.json
├── index.html
├── src/
├── public/
├── server/
└── shared/
```

## Environment setup

No API keys, passwords, tokens, database credentials, or `.env` values are required. The dashboard is a static-data application; the validated dataset is embedded in `src/data.ts` for reproducible local execution.

## Important configuration

`vite.config.ts` uses the repository-local `src/` directory as the Vite root and `@` as the source alias. The production build writes to `dist/public`; generated build output and `node_modules` are excluded by the root `.gitignore`.
