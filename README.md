# 🏦 Insurance Policy Analytics Dashboard

> End-to-end Power BI dashboard covering the complete insurance 
> policy lifecycle — built to give leadership, finance, 
> and sales teams a single unified view of portfolio performance.

---

## 📌 Project Background

This project was built to solve a real problem — sales teams 
and leadership working from different numbers, with no 
consolidated view of the business and no forward-looking 
visibility into payment obligations.

The goal: one dashboard that covers everything from policy 
creation through to maturity, useful for everyone from a 
frontline sales agent to the CEO.

> ⚠️ Note: Data has been anonymized. The logic, data model, 
> DAX calculations, and design are original work.

---

## 🗂️ Dashboard Pages

| Page | Business Question Answered |
|------|---------------------------|
| Summary | Where does the business stand right now? |
| Insurance Overview | How is the portfolio performing across all dimensions? |
| Investment Value | Is the money customers invest generating good returns? |
| Protection Value | What is the gap between premiums paid and coverage provided? |
| Premium Analysis | What do our payment obligations look like going forward? |
| Sales Hierarchy | Who is performing, at what level, and where do we focus? |

---

<img width="1276" height="575" alt="image" src="https://github.com/user-attachments/assets/195ad252-4768-4ac5-9368-d9ad5297c05d" />

---

<img width="1249" height="712" alt="image" src="https://github.com/user-attachments/assets/7967264f-49ae-43cb-abac-1c93ae938579" />

---

<img width="1257" height="620" alt="image" src="https://github.com/user-attachments/assets/befe27f5-f908-49ac-b4df-721ac309e060" />

---

<img width="1250" height="731" alt="image" src="https://github.com/user-attachments/assets/1c4da356-8542-46bc-8dfc-c0b836706169" />

---
<img width="1233" height="705" alt="image" src="https://github.com/user-attachments/assets/db7e6212-4406-4703-ab10-9707baa82434" />


## 🔧 Technical Approach

### Data Model
- Snowflake schema — fact table in center, 
  dimension tables branching out
- Tables: Customer Detail, Insurance Agent Sales, 
  Policy Type, Policy Protection Plan, 
  Regional Manager, Zonal Manager, Fact Table
- Bidirectional filter relationships on sales hierarchy 
  dimensions to support drill-down correctly

### Power Query
- Custom date transformation to fix inconsistent 
  text-based date formats across source fields
- Calendar table validation
- Calculated columns for payment duration 
  and derived date fields

### DAX Measures
- Total Premium Amount
- Total Annual Premium
- Total Premium Paid / Payable
- Underwriting Expense
- Annualized ROI (CAGR formula)
- Profit and Gain
- Annual Amount Growth
- Payment Bucket (calculated column 
  for forward-looking liability grouping)

---

## ⭐ Key Features

**Field Parameters — Dynamic Metric Switcher**
Sales team kept requesting different metrics every week. 
Built a field parameter dropdown that switches all six 
charts on the Insurance Overview page simultaneously. 
One dropdown. Any metric. No rebuilding.

**Payment Bucket — Forward Looking Liability View**
Finance team had no way to see upcoming payment obligations. 
Created a DAX calculated column grouping active policies 
by when remaining premiums fall due — within 5 years, 
5-10, 10-15, 15-20. Turned historical reporting 
into financial planning.

**Row Level Security — Organization-Wide Deployment**
Implemented RLS roles in the data model from day one:
- Sales Agent → own data only
- Regional Manager → own region only  
- Zonal Manager → own zone only
- Owner → full view

Same dashboard. Right data for every person.

**Sales Hierarchy Drill-Down**
Four-click navigation from Zonal Manager → 
Regional Manager → Sales Agent → Customer. 
Toggle between matrix and chart view.

---

## 📊 Key Insights

- Annualized ROI grew consistently over 10 years — 
  strong product quality signal
- Protection gap widening — customers getting more 
  coverage relative to premiums paid, positive for retention
- Significant payment obligations concentrated 
  in the near-term window — critical for finance planning

---

## 🛠️ Tools Used

- **Power BI Desktop** — data model, DAX, report design
- **Power Query (M)** — data transformation and cleaning
- **DAX** — measures, calculated columns, field parameters
- **Row Level Security** — data governance layer

---

## 👤 Author

**Vignesh Subramaniam**  
[LinkedIn](https://linkedin.com/in/vignesh2912) · 
[GitHub](https://github.com/vickythatguy)

---

## 📁 Files

| File | Description |
|------|-------------|
| `Insurance_Dashboard.pbix` | Main Power BI file |
| `README.md` | Project documentation |
