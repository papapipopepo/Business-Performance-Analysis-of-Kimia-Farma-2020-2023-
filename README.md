# 📊 Kimia Farma Big Data Analytics (Final Task – Rakamin Academy)

This project analyzes the business performance of **Kimia Farma** from **2020 to 2023** using **Google BigQuery** and **Looker Studio**. The goal is to extract insights from transactional data and deliver a comprehensive, interactive dashboard for decision-making.

---

## 📁 Dataset Description

Imported datasets (in CSV format):

| File Name              | Description                                 |
|------------------------|---------------------------------------------|
| `kf_final_transaction` | Transactional data (date, price, discount)  |
| `kf_product`           | Product info (name, price, ID)              |
| `kf_kantor_cabang`     | Branch location & rating                    |
| `kf_inventory`         | Inventory stock levels (not used in viz)    |

---

## 🛠️ Data Processing

All data were imported to BigQuery. A consolidated analysis table was created using SQL JOIN and calculated fields:

- `nett_sales` = `price * (1 - discount_percentage / 100)`
- `nett_profit` = `nett_sales * gross margin %`
- `gross_margin %` assigned using `CASE WHEN` based on price tiers:
  - ≤ 50,000 → 10%
  - ≤ 100,000 → 15%
  - ≤ 300,000 → 20%
  - ≤ 500,000 → 25%
  - > 500,000 → 30%

---

## 📊 Dashboard Highlights (Looker Studio)

Key components visualized:

- ✅ Total transactions, net sales, nett profit, total products, average rating
- 📈 Yearly revenue trends (2020–2023)
- 📍 Top 10 provinces by transaction & sales
- 🏢 Branches with high internal rating but low customer rating
- 🗺️ Profit map across Indonesian provinces
- 📆 Monthly revenue trends
- 💸 Top 5 most profitable products
- 🔍 Interactive filters by province, city, and branch

---

## 🧾 Tools Used

- **Google BigQuery** – Data warehouse and SQL processing
- **Looker Studio** – Data visualization and dashboarding
- **Google Cloud Platform** – Storage and infrastructure

---

## 📷 Screenshots

![Dashboard Preview](d![Image](https://github.com/user-attachments/assets/ee546720-c423-41f7-9ffb-14ec111d1f04))

---

## 👨‍💻 Author

**Ezra Satria Bagas Airlangga**  
Fast Track Master’s Student – Electrical Engineering, Telkom University  
[LinkedIn](https://linkedin.com/in/ezrasatriabagas/)  
