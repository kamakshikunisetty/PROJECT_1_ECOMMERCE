# Customer Experience & E-Commerce Performance Investigation

An end-to-end e-commerce analytics project using **SQL, Python, Power BI, and GenAI/NLP** to investigate customer experience, delivery performance, customer feedback, seller/category exposure, and operational investigation priorities.

## Project Overview

This project analyzes the **Olist Brazilian E-Commerce Public Dataset** to understand how operational and customer-experience signals interact across the e-commerce journey.

The analysis follows the journey:

**Customer → Order → Seller → Product → Delivery → Review**

Rather than treating customer satisfaction as a single KPI, the project investigates:

- Delivery performance and customer satisfaction
- Customer reviews and complaint themes
- Seller-level business exposure and experience metrics
- Product-category performance
- Geographic delivery signals
- Customer repeat-purchase behavior
- Statistical evidence and effect sizes
- Operational investigation priorities
- KPI monitoring recommendations

The final Power BI dashboard consists of **6 analytical pages**, moving from executive overview to investigation and action.

---

## Business Questions

1. How healthy is the overall customer experience?
2. How does delivery performance relate to customer satisfaction?
3. What are customers saying and what operational signals appear behind complaints?
4. Which sellers and product categories combine meaningful business exposure with weaker observed experience?
5. What evidence supports further investigation?
6. What should the business investigate next and how should progress be measured?

---

## Dashboard Story

### 01 — Executive Overview
Provides the overall view of e-commerce performance and customer experience.

### 02 — Delivery Experience
Investigates the relationship between delivery severity and customer satisfaction.

### 03 — Customer Voice
Analyzes customer ratings, written reviews, complaint themes, and directional NLP/sentiment signals.

### 04 — Seller & Product Performance
Identifies sellers and categories where business exposure overlaps with weaker observed customer-experience metrics.

### 05 — Investigation & Action Center
Brings together statistical evidence, hypotheses, investigation priorities, and business interpretation.

### 06 — Action Center
Converts the evidence into operational investigation areas and a KPI monitoring framework.

---

## Key Findings

### Delivery Performance

Delivery delay showed the strongest tested association with customer satisfaction in the analysis.

- Kruskal-Wallis H = **8637.20**
- p < **0.001**
- ε² ≈ **0.0901**
- n = **95,824**

Median review scores varied substantially across delivery-severity groups.

This result is treated as an **association**, not proof of causation.

### Seller Exposure

The seller segmentation identified:

- **314** high-revenue / lower-experience sellers
- Approximately **40.21%** of seller-segment revenue exposure

These sellers had weaker observed experience metrics than the high-revenue / high-experience comparison group.

The segmentation is used to identify **investigation priorities**, not confirmed root causes.

### Category Exposure

The analysis identified **11 categories** classified as high-revenue / lower-experience based on the project's segmentation criteria.

These categories provide areas for further investigation into fulfillment, product, or service-related operational signals.

### Customer Voice

Customer review text was analyzed using a directional complaint-screening approach and exploratory NLP validation.

The complaint sample is **directional rather than population-representative**, so complaint counts are not presented as whole-dataset complaint rates.

### Repeat Purchase

The 90-day customer journey analysis found **no clear difference** in repeat-purchase rates across positive, neutral, and negative reviewed experience groups within the observable period.

This prevents the analysis from making an unsupported claim that poorer reviews directly reduce repeat purchasing.

---

## Statistical Evidence

| Hypothesis | Method | Result | Interpretation |
|---|---|---|---|
| Delivery delay ↔ satisfaction | Kruskal-Wallis | p < 0.001, ε² ≈ 0.0901 | Strongest tested association |
| Distance ↔ satisfaction | Kruskal-Wallis | p < 0.001, ε² ≈ 0.0044 | Weak association |
| Freight ratio ↔ satisfaction | Kruskal-Wallis | p < 0.001, ε² ≈ 0.00066 | Very weak association |
| Order value ↔ satisfaction | Kruskal-Wallis | p < 0.001, ε² ≈ 0.0018 | Very weak association |
| Experience ↔ 90-day repeat purchase | 90-day comparison | Similar reviewed-group rates | No clear difference observed |

---

## Technology Stack

### Data & Analysis
- Python
- Pandas
- NumPy
- Scikit-learn
- Statistical analysis

### Database
- SQL
- MySQL

### Business Intelligence
- Microsoft Power BI
- DAX
- Data modeling
- Interactive dashboards

### NLP / GenAI
- Exploratory NLP
- Sentiment validation
- Complaint-theme classification
- GenAI-assisted analysis

### Development & Version Control
- Jupyter Notebook
- Git
- GitHub

---

## Project Structure

```text
PROJECT_1_ECOMMERCE/
│
├── data/
│   └── Dataset and processed data
│
├── documentation/
│   └── PROJECT_STORY.md
│
├── nlp/
│   └── NLP and customer-feedback analysis
│
├── notebooks/
│   └── Python analysis notebooks
│
├── presentation/
│   └── Project presentation materials
│
├── powerbi/
│   └── Power BI dashboard
│
├── screenshots/
│   └── Dashboard screenshots
│
├── sql/
│   └── SQL analysis and queries
│
└── README.md