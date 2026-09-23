# Customer Experience & E-Commerce Performance Investigation

## Project Overview

This project investigates customer experience and e-commerce performance using the Olist Brazilian E-Commerce Public Dataset.

The analysis combines:

- SQL
- Python
- Exploratory Data Analysis
- Statistical Analysis
- NLP / GenAI-assisted customer voice analysis
- Power BI
- Business Analysis

The objective is not simply to report sales metrics, but to investigate how delivery performance, customer reviews, seller exposure, product categories, and customer behavior interact within the observed dataset.

---

# Business Question

How can e-commerce customer experience be investigated using operational, customer, seller, product, and behavioral data?

The analysis follows this progression:

**Overall Performance → Delivery Experience → Customer Voice → Seller & Product Performance → Evidence & Investigation → Action & Measurement**

---

# Dataset

The project uses the Olist Brazilian E-Commerce Public Dataset.

The dataset contains information related to:

- Customers
- Orders
- Order items
- Products
- Sellers
- Payments
- Reviews
- Geographical information

The analysis covers the observed period:

**2016–2018**

---

# Analytical Approach

The project was developed as an end-to-end analytics workflow.

## 1. Data Preparation

The source data was examined, cleaned, transformed, and structured for analysis.

Key areas included:

- Order-level information
- Customer information
- Seller information
- Product categories
- Delivery dates
- Review scores
- Review text
- Payment information
- Freight and order-value metrics

---

# 2. SQL Analysis

SQL was used to investigate the underlying business data and create analytical datasets.

The analysis focused on:

- Order performance
- Customer experience
- Seller performance
- Product/category performance
- Delivery behavior
- Review patterns
- Customer journey relationships

---

# 3. Python Analysis

Python was used for deeper analysis and statistical investigation.

Key activities included:

- Data cleaning
- Exploratory analysis
- Feature engineering
- Customer-level analysis
- Seller segmentation
- Category segmentation
- Statistical testing
- Effect-size analysis
- Customer journey analysis

---

# 4. Customer Voice / NLP

Customer review text was investigated to identify recurring complaint themes.

A screening sample of written reviews was categorized to provide directional customer-voice context.

The complaint analysis identified potential themes such as:

- Delivery
- Product
- Payment
- Seller/service
- Other operational issues

The complaint screening is treated as **directional evidence rather than a population-representative complaint rate**.

An additional Portuguese sentiment validation exercise was performed using a balanced sample of reviews.

The NLP output was treated as exploratory validation rather than ground truth.

---

# 5. Power BI Investigation

The Power BI dashboard presents the investigation as a six-page analytical story.

---

## Page 1 — EXECUTIVE OVERVIEW

### Business Question

**How healthy is the overall customer experience?**

This page establishes the overall business and customer-experience context.

It provides the starting point for the investigation before moving into specific operational drivers.

---

## Page 2 — DELIVERY EXPERIENCE

### Business Question

**How does delivery performance relate to customer satisfaction?**

Delivery performance was investigated using delivery-severity groups and customer review scores.

The statistical analysis produced:

- Kruskal-Wallis H = 8637.20
- p < 0.001
- ε² ≈ 0.0901
- n = 95,824

The analysis indicates a meaningful association between delivery delay severity and customer satisfaction within the observed data.

The result is treated as an **association rather than proof of causation**.

Delivery severity showed the strongest tested customer-experience association in this investigation.

---

## Page 3 — CUSTOMER VOICE

### Business Question

**What are customers saying, and where do complaint signals point to operational issues?**

This page combines:

- Review-score distribution
- Negative-review rate
- Review trends
- Complaint themes
- Complaint themes by rating
- Complaint-to-operational signals
- NLP validation

The complaint screening used a sample of written reviews.

Therefore, complaint counts are used to identify **investigation signals**, not to claim whole-dataset complaint rates.

The NLP validation was also treated as exploratory evidence.

---

## Page 4 — SELLER & PRODUCT PERFORMANCE

### Business Question

**Where does business exposure overlap with weaker customer experience?**

Seller and category segmentation was used to identify areas where meaningful business exposure overlaps with weaker observed experience metrics.

### Seller Segmentation

Using a minimum review-volume threshold:

- 314 sellers were classified as **High Revenue + Lower Experience**
- These sellers represented approximately **40.21% of seller-segment revenue exposure**

Their observed metrics included:

- Average rating: approximately 3.883
- Negative review rate: approximately 19.34%
- Late delivery rate: approximately 9.91%

These results identify areas for investigation rather than confirmed operational causes.

### Category Segmentation

Using a minimum review-volume threshold:

- 11 categories were classified as **High Revenue + Lower Experience**

These categories provide another layer for investigating where customer experience signals overlap with meaningful business exposure.

---

## Page 5 — INVESTIGATION & ACTION CENTER

### Business Question

**What evidence should the business investigate further, and what actions and KPIs should be monitored?**

This page brings together the main analytical evidence.

The investigation compared multiple hypotheses:

| Hypothesis | Evidence | Interpretation |
|---|---|---|
| Delivery delay ↔ satisfaction | p < 0.001, ε² ≈ 0.0901 | Strongest tested association |
| Distance ↔ satisfaction | p < 0.001, ε² ≈ 0.0044 | Weak association |
| Freight ratio ↔ satisfaction | p < 0.001, ε² ≈ 0.00066 | Very weak association |
| Order value ↔ satisfaction | p < 0.001, ε² ≈ 0.0018 | Very weak association |
| Negative experience ↔ repeat purchase | Similar 90-day rates | No clear difference |

The page then translates these findings into investigation priorities across:

- Delivery
- Sellers
- Categories
- Geography
- Customer complaints

---

# 6. ACTION CENTER

### Business Question

**What should the business investigate next, and how will progress be measured?**

The final page converts the investigation into an operational monitoring framework.

## Delivery Operations

Investigate late-delivery patterns by:

- Seller
- Geography
- Category

Relevant KPIs:

- Late Delivery Rate
- Average Review Score

Evidence:

**ε² ≈ 0.0901, p < 0.001**

---

## Seller Exposure

Investigate high-revenue sellers with lower observed experience metrics.

Relevant KPIs:

- Negative Review Rate
- Late Delivery Rate
- Average Review Score

The purpose is to identify seller-level operational opportunities within meaningful business exposure.

---

## Category & Customer Voice

Investigate high-revenue/lower-experience categories together with recurring customer complaint themes.

Relevant KPIs:

- Average Review Score
- Late Delivery Rate
- Complaint Mentions
- Negative Review Rate

Complaint themes are used as directional customer-voice evidence.

---

# Important Negative Finding

A 90-day customer journey analysis tested whether reviewed customer experience groups showed different repeat-purchase behavior.

The observed repeat rates were:

- Positive: 2.1579%
- Negative: 2.1392%
- Neutral: 2.1090%
- No Review: 5.7566%

The reviewed positive, negative, and neutral groups showed very similar repeat-purchase rates.

Therefore, the analysis does **not** make a claim that poorer observed customer experience reduces repeat purchase within the 90-day observation window.

This is an important example of allowing the data to constrain the conclusion rather than forcing a business narrative.

---

# Key Findings

## 1. Delivery Performance

Delivery delay showed the strongest tested association with customer satisfaction.

This makes delivery performance an important area for operational investigation.

---

## 2. Seller Exposure

314 high-revenue/lower-experience sellers represented approximately 40.21% of seller-segment revenue exposure.

This identifies meaningful business exposure where further seller-level investigation may be useful.

---

## 3. Category Exposure

11 categories showed the combination of meaningful revenue exposure and lower observed experience metrics.

These categories can be investigated for category-specific fulfillment, product, or service issues.

---

## 4. Customer Voice

Customer review text provides additional operational context through recurring complaint themes.

However, the complaint screening sample is directional and should not be interpreted as representative of all customers.

---

## 5. Repeat Purchase

The 90-day analysis did not show a clear difference in repeat-purchase rates across positive, neutral, and negative reviewed groups.

This prevents an unsupported retention conclusion.

---

# Statistical Interpretation

The analysis distinguishes between:

- Statistical significance
- Effect size
- Association
- Causation

A statistically significant result does not automatically imply a practically large relationship.

For example, distance, freight burden, and order value showed statistically significant relationships with satisfaction but substantially smaller effect sizes than delivery delay.

Therefore, the investigation prioritizes effect size and business relevance alongside statistical significance.

---

# Business Interpretation

The overall investigation suggests that customer experience should be examined through multiple connected layers:

**Customer → Order → Seller → Product → Delivery → Review**

Delivery performance provides the strongest tested customer-experience signal.

Seller and category segmentation then identifies where weaker observed experience overlaps with meaningful business exposure.

Customer voice provides additional operational context.

The resulting framework is designed to support further operational validation rather than claim confirmed root causes.

---

# Recommended Investigation Framework

The recommended workflow is:

**OBSERVATION → EVIDENCE → BUSINESS IMPLICATION → INVESTIGATION → KPI MONITORING**

The dashboard therefore focuses on identifying evidence-backed areas for further investigation rather than prescribing unsupported causal explanations.

---

# Limitations

The analysis has several important limitations:

1. The dataset is observational.
2. Statistical association does not establish causation.
3. Complaint analysis uses a screening sample rather than the complete review population.
4. NLP sentiment analysis is exploratory.
5. Seller and category segmentation depends on review-volume thresholds.
6. Geographic signals are treated as hotspot candidates rather than confirmed causes.
7. The 90-day repeat-purchase analysis is limited to the observable customer journey window.

These limitations are explicitly reflected in the dashboard interpretation.

---

# Final Takeaway

Delivery performance is the clearest tested customer-experience signal.

Seller and category segmentation shows where weaker observed experience overlaps with meaningful business exposure, while customer voice provides directional operational context.

The next step is not to assume a root cause, but to validate these signals through seller-, category-, geography-, and delivery-level operational investigation and monitor whether the associated KPIs change over time.

---

# Tools & Technologies

- SQL
- Python
- Pandas
- NumPy
- Scikit-learn
- Statistical Analysis
- NLP / GenAI
- Power BI
- DAX
- Git / GitHub

---

# Project Structure

```text
PROJECT_1_ECOMMERCE/
│
├── data/
├── documentation/
│   └── PROJECT_STORY.md
├── nlp/
├── notebooks/
├── presentation/
├── powerbi/
├── screenshots/
└── sql/