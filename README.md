# SuperMarket Data Analytics

**Student:** ChandhraShekhar  
**Program:** IBM SkillsBuild Data Analytics with AI Academic Internship Program

This repository contains the complete internship project built from the supplied `SUPERMARKETDATA-dataanyliticsprojectdataset.pdf`. It follows **DATA → INFORMATION → INSIGHT → DECISION → ACTION** and uses the supermarket dataset as the single source of truth.

## Repository structure

```text
SuperMarketDataAnalytics/
├── README.md
├── requirements.txt
├── SuperMarketDataAnalytics.ipynb
├── SuperMarketDataAnalytics_ProjectReport.docx
├── dataset/
│   └── supermarket_data.csv
└── web_application/
    ├── README.md
    ├── requirements.txt / package.json
    ├── src/
    ├── public/
    └── other Vite/TypeScript files
```

## Dataset validation

The extracted dataset contains **500 records and 13 columns**: Invoice ID, Date, Branch, City, Customer Type, Gender, Product, Category, Quantity, Unit Price, Payment, Rating, and Sales. Validation found **0 missing values, 0 duplicate rows, 0 duplicate invoice IDs, and 0 Sales formula mismatches**. Sales was checked against Quantity × Unit Price.

## Notebook and report

`SuperMarketDataAnalytics.ipynb` contains data loading, cleaning, validation, KPI calculation, exploratory analysis, category/product analysis, city/branch analysis, customer analysis, payment analysis, rating analysis, and evidence-led business insights.

`SuperMarketDataAnalytics_ProjectReport.docx` documents the method, calculated results, limitations, findings, and recommended actions.

## Predictive modeling decision

Sales prediction was not used because Sales is deterministically derived from Quantity × Unit Price. An exploratory Rating model was evaluated separately; it did not outperform the mean baseline, so the final project keeps the primary workflow analytics-first rather than presenting an unhelpful model as business intelligence.

## Run the notebook

```bash
pip install -r requirements.txt
jupyter notebook SuperMarketDataAnalytics.ipynb
```

## Run the web application

```bash
cd web_application
pnpm install
pnpm dev
```

The web application contains the validated supermarket data in `web_application/src/data.ts`, generated from `dataset/supermarket_data.csv`. It includes synchronized city, branch, category, and customer-type filters and sections for Executive Overview, Sales & Products, Customer Analysis, Branch & City Analysis, Payment Analysis, Rating Analysis, and Business Insights.

## Key calculated results

- Total Sales: **₹244,411.08**
- Quantity sold: **2,768 units**
- Average transaction: **₹488.82**
- Average rating: **3.99 / 5**
- Leading category: **Beverages**
- Leading product: **Cheese**
- Leading city: **Mumbai**
- Most frequent payment method: **UPI**

## Dataset source

**Dataset Source: To be added manually.** The supplied PDF did not include a source URL. This is the one manual item to complete before internship submission if the original source link is available.

## Limitations

The dataset is a static six-month extract and does not include margin, inventory, promotions, payment failures, or longitudinal customer history. Associations are not treated as causal effects.

## Future Scope

Future extensions could add a validated date-range filter, inventory and margin fields, payment-failure data, longer customer history, and a genuine future outcome target before introducing predictive modeling.
