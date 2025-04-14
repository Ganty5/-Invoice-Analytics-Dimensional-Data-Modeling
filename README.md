# Invoice-Based Dimensional Modelling Project
![image](https://github.com/user-attachments/assets/5c03b588-9edc-4d07-8138-92187f63af8b)

This project transforms a raw invoice dataset into a robust, scalable dimensional model using the star schema approach. It was completed as part of the HNG Stage 8 Internship and focuses on structuring sales data for efficient reporting and deep analytics.

## 🧩 Project Overview

- **Business Focused**: The dataset was analyzed to answer essential questions—who bought what, when, and where.
- **Star Schema Design**: Built around a central `fact_sales` table with four dimension tables: `dim_customer`, `dim_product`, `dim_store`, and `dim_time`.
- **Grain**: One row per product per invoice line item, allowing granular drill-downs.
- **Degenerate Dimension**: `Invoice_ID` is stored in the fact table for tracking purposes without redundancy.
  
## 🛠️ Dimensional Modeling Strategy

- **Star Schema** improves clarity, reduces joins, and enhances query speed.
- ![image](https://github.com/user-attachments/assets/c2fb20eb-3eef-42da-bc9a-e9ff3623e830)

- Dimension tables support slicing data by customer, product, store, and time.
- ![image](https://github.com/user-attachments/assets/6761f33b-a070-48e6-b251-44ac24a7ef0d)
- 
- Designed with business reporting and trend analysis in mind.

## 🔄 SCD Handling
![image](https://github.com/user-attachments/assets/bcf1130f-5f9e-4c25-a1e3-bae94077f0dc)

- Type 2 used for `dim_customer` and `dim_store` to track historical changes.
- Type 1 or 2 applied to `dim_product` depending on price volatility.
- No changes needed for `dim_time`.

## ⚙️ ETL Pipeline

Structured ETL flow with four stages:
![image](https://github.com/user-attachments/assets/a91c179d-cd74-4fd5-a112-afe979e5332f)

1. **Extract** – Load raw invoice data (CSV or API).
2. **Transform** – Clean, enrich, and apply SCD logic.
3. **Load** – Populate fact and dimension tables.
4. **Quality Checks** – Ensure uniqueness, referential integrity, and consistency.


## 📈 Advanced Features

- Built-in time hierarchy (day → month → year) and store/product breakdowns.
- Uses surrogate keys and indexing for performance.
- Supports incremental data loading to reduce processing time.

## 🧠 Scalability & Future Enhancements

- Can be extended with new dimensions (e.g., payment methods, regions).
- Supports integration with ML tools for predictive insights.
- Ready for production-grade reporting and trend monitoring.

---

### 🔍 Tools Used

- SQL & Python (Pandas)
- Power BI (optional for dashboarding)
- Conceptual modeling with Star Schema

---

### 📌 Author

**Chidinma Ukandu**  
MSc Business Intelligence | HNG Internship Stage 8 Finalist  
[LinkedIn](your_link) | [Portfolio](your_link)
