# Brazilian E-Commerce Sales and Delivery Analytics

## Project Overview

This project analyzes the Olist Brazilian E-Commerce Dataset using Python and Tableau. The goal is to study sales performance, revenue, customer behavior, product performance, delivery efficiency, and review patterns across the marketplace.

The dataset contains multiple CSV files related to customers, orders, products, sellers, reviews, payments, geolocation, and category translation. These files are combined and transformed into analysis-ready tables for business exploration and dashboarding.

## Business Goals

The project is designed to answer questions such as:

- Which states, cities, sellers, and product categories generate the most revenue?
- Which products sell the most and which categories are growing or declining?
- Which sellers and regions have late deliveries or poor customer ratings?
- How do monthly sales, revenue, and customer ratings change over time?
- Which payment methods are most used by customers?
- Which products or categories may need marketing support or operational improvement?

## Dataset Files

The raw project data is organized as follows:

- `dataset/olist_customers_dataset.csv`
- `dataset/olist_orders_dataset.csv`
- `dataset/olist_order_items_dataset.csv`
- `dataset/olist_order_payments_dataset.csv`
- `dataset/olist_order_reviews_dataset.csv`
- `dataset/olist_products_dataset.csv`
- `dataset/olist_sellers_dataset.csv`
- `dataset/olist_geolocation_dataset.csv`
- `dataset/product_category_name_translation.csv`

## Tools Used

- Python
- pandas
- numpy
- matplotlib
- seaborn
- Tableau

## Notebook Workflow

The main notebook, `DataAnalytics1.ipynb`, performs the full analysis pipeline:

1. Import required libraries.
2. Load all dataset files.
3. Inspect dataset shape, missing values, duplicate rows, and statistical summary.
4. Clean and transform the data.
5. Convert timestamps and engineer delivery features.
6. Merge customer, order, product, seller, payment, and review tables.
7. Perform grouping and aggregation for revenue, sales volume, ratings, and delivery metrics.
8. Build trend analysis for monthly sales and revenue.
9. Create visualizations for dashboards and reporting.
10. Export cleaned analysis-ready datasets for Tableau.

## Key Analysis Tables

The notebook creates several analysis-ready tables:

- `order_base`: one row per order with customer, payment, delivery, and review fields.
- `item_base`: one row per order item with product, seller, category, and review fields.
- `tableau_full`: a denormalized export with one row per order-item and all key analytical fields.

These tables are built to support both Python analysis and Tableau dashboards.

## Outputs Generated

The project creates these cleaned or analysis-ready files:

- `cleaned_olist_dataset.csv`
- `cleaned_olist_order_level.csv`
- `cleaned_olist_item_level.csv`
- `olist_tableau_full_dataset.csv`

These outputs are useful if you want to build dashboards directly in Tableau without re-running the notebook.

## Tableau Usage

To use this project in Tableau:

1. Open Tableau Desktop or Tableau Public.
2. Connect to `olist_tableau_full_dataset.csv`.
3. Use `month`, `customer_state`, `customer_city`, `category`, `seller_state`, `seller_city`, `payment_type`, `review_score`, `delivery_days`, and `delivery_delay` as analysis fields.
4. Build dashboards for revenue, sales volume, customer satisfaction, delivery delay, and regional performance.

## Example Business Insights

The dataset supports insights such as:

- High-revenue categories and sellers.
- States and cities with strong sales concentration.
- Categories with low review scores or expensive shipping.
- Sellers and regions with delayed deliveries.
- Payment behavior and customer preference patterns.
- Monthly sales and revenue trends over time.

## Project Structure

```text
Data Analytics 1/
├── DataAnalytics1.ipynb
├── DataAnalytics.twb
├── README.md
├── cleaned_olist_dataset.csv
├── cleaned_olist_order_level.csv
├── cleaned_olist_item_level.csv
├── olist_tableau_full_dataset.csv
└── dataset/
	├── olist_customers_dataset.csv
	├── olist_geolocation_dataset.csv
	├── olist_orders_dataset.csv
	├── olist_order_items_dataset.csv
	├── olist_order_payments_dataset.csv
	├── olist_order_reviews_dataset.csv
	├── olist_products_dataset.csv
	├── olist_sellers_dataset.csv
	└── product_category_name_translation.csv
```

## How To Reproduce

1. Open `DataAnalytics1.ipynb` in Jupyter or VS Code.
2. Run the notebook cells from top to bottom.
3. Review the analysis tables, charts, and summary outputs.
4. Use the exported CSV files in Tableau for dashboard creation.

## Notes

- The Olist dataset is split across multiple CSV files, so the analysis relies on merging them into order-level and item-level tables.
- The Tableau export is denormalized for easier dashboarding.
- Some business metrics are computed at the order level, while others are computed at the item level for better accuracy.

## Authoring Goal

This project was created to demonstrate end-to-end data analytics work: loading, cleaning, transformation, aggregation, visualization, and dashboard-ready export for a real e-commerce dataset.
