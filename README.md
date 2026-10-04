# 👥 Customer RFM Segmentation + Lifetime Value Analysis
## Data Analytics Portfolio Project

**By:** Priyanshu | B.Tech CSE-AIML, MDU Rohtak  
**Analysis Type:** Customer Segmentation & Lifetime Value  
**Dataset:** 4,312 customers | £8.8M revenue | 19,213 orders | 2009-2010
📄 Full findings write-up: [BUSINESS_INSIGHTS.md](BUSINESS_INSIGHTS.md)


---

## 🎯 PROJECT OVERVIEW

This project demonstrates **customer segmentation analysis** using the RFM (Recency, Frequency, Monetary) framework and Customer Lifetime Value (CLV) analysis.

**What the analysis reveals:**
- How customers are distributed across value tiers
- Why some customers are more valuable than others
- Clear patterns in customer behavior and retention
- The relationship between customer age and spending

---


## Dashboard Preview

### RFM Segmentation Dashboard
![RFM Dashboard](Visuals/RFM%20Customer%20Segementation%20Analysis.png)

### Customer Lifetime Value Dashboard
![CLV Dashboard](Visuals/Customer%20Lifetime%20Value%20Analysis.png)

### Retention Analysis Dashboard
![Retention Dashboard](Visuals/Customer%20Retention%20Analysis.png)

## 📊 THE DATA

**Dataset:** Online Retail II (E-commerce transactions)
- **4,312 customers** analyzed
- **19,213 orders** examined
- **£8,832,003** total revenue
- **407,664 transactions** processed
- **Time period:** December 2009 - December 2010

**Note on the raw dataset:** `online_retail_II.xlsx` (44MB) isn't committed to this
repo to keep it lightweight. Download it directly from the source:
[UCI Machine Learning Repository — Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
and place it in `Data/` to re-run `Notebook/customer_analytics.ipynb` yourself.
---

## 📈 KEY FINDINGS

### Finding 1: Customer Concentration

| Segment | Count | % of Customers | Revenue | % of Revenue | Avg CLV |
|---------|-------|----------------|---------|--------------|---------|
| Champions | 926 | 21% | £5.7M | **64.87%** | £35K |
| Loyal | 973 | 23% | £1.3M | 14.88% | £24K |
| At-Risk | 688 | 16% | £1.0M | 11.8% | £8K |
| New | 1,358 | 32% | £561K | 6.36% | £2K |
| Potential | 367 | 8% | £185K | 2.1% | £10K |

**Key Insight:** Champions (just 21% of your customers) generate nearly 65% of your revenue.

---

### Finding 2: New Customer Retention

**Actual retention by cohort month:**

| Metric | Value |
|--------|-------|
| Month 1 | 100% (baseline) |
| Month 2 | ~21% return (79% don't) |
| Month 3 | ~25% engaged |
| Month 6 | ~27% engaged |
| Month 12 | ~15% engaged |
| **Overall Retention** | **35% average** |

**Key Insight:** Most customers don't make a second purchase. 85% of new customers churn by month 12.

---

### Finding 3: Customer Value Increases Over Time

**CLV by customer age:**
- 0-30 days: £2K (New)
- 31-90 days: £5K
- 91-180 days: £12K
- 181-365 days: £24K (Loyal)
- 365+ days: £35K (Champions)

**Key Insight:** Customers who stay longer spend significantly more over their lifetime. Champions spend 17x more than new customers.

---

### Finding 4: RFM Framework Predicts Value

**Average RFM Scores by Segment:**

| Segment | R Score | F Score | M Score | CLV |
|---------|---------|---------|---------|-----|
| Champions | 4.6 | 4.7 | 4.6 | £35K |
| Loyal | 3.7 | 3.6 | 3.3 | £24K |
| Potential | 4.3 | 1.6 | 2.0 | £10K |
| At-Risk | 1.7 | 3.3 | 3.1 | £8K |
| New | 1.8 | 1.5 | 1.8 | £2K |

**Key Insight:** High RFM scores accurately predict high customer value.

---

### Finding 5: Retention Distribution

- **Low Retention:** 82.42% of cohorts
- **High Retention:** 14.29% of cohorts
- **Average retention rate:** 35%
- **Average customer tenure:** 5 months

**Key Insight:** Most customer cohorts struggle to retain beyond month 2.

---

## Business Recommendations

### Champions
- Launch VIP loyalty programs
- Provide exclusive offers
- Prioritize retention efforts

### At-Risk Customers
- Trigger win-back campaigns
- Offer personalized discounts
- Re-engage through email marketing

### New Customers
- Improve onboarding experience
- Encourage second purchase within 30 days
- Use targeted promotional campaigns

---

## 🔍 METHODOLOGY

**A note on CLV scope:** CLV is calculated as `AvgOrderValue × Frequency × (CustomerAgeDays / 30)`.
This returns exactly 0 for any customer whose first and last purchase happen on the same
calendar day — mostly one-time buyers — so those ~1,500 customers are excluded from every
CLV-based figure in this report. RFM metrics (which don't use this formula) still cover all
4,312 customers. Full detail is in `Notebook/customer_analytics.ipynb`, Section 6.

### RFM Segmentation

**Recency:** Days since last purchase (1-5 scale)
- 5 = most recent buyer
- 1 = haven't bought recently

**Frequency:** Number of purchases (1-5 scale)
- 5 = most frequent buyer
- 1 = rare buyer

**Monetary:** Total spending (1-5 scale)
- 5 = highest spender
- 1 = lowest spender

### The 5 Segments Created

1. **Champions** (926 customers)
   - High on all three metrics
   - Recent, frequent, high-value buyers

2. **Loyal Customers** (973 customers)
   - Good on most metrics
   - Regular, reliable buyers

3. **Potential Loyalists** (367 customers)
   - Recent activity, building engagement
   - Early-stage customers

4. **At-Risk Customers** (688 customers)
   - Low recency (haven't bought in months)
   - But high historical frequency/spending
   - Dormant but historically valuable

5. **New Customers** (1,358 customers)
   - Newest segment
   - Haven't repeated purchase
   - Lowest value

---

## Technical Implementation

- Data cleaning and preprocessing in Python
- Missing value treatment
- RFM score calculation using quintiles
- Customer segmentation logic
- CLV estimation
- Cohort retention matrix generation
- Power BI dashboard development

---

## 🛠️ TOOLS & TECHNOLOGIES USED

**Python** (Data Analysis)
- Pandas for data manipulation
- NumPy for calculations
- Matplotlib/Seaborn for visualization

**Power BI** (Dashboards)
- Interactive segmentation dashboard
- CLV analysis dashboard
- Retention tracking dashboard
- DAX measures and slicers

**Analytics Methodology**
- RFM Segmentation
- Cohort Analysis
- Customer Lifetime Value Calculation
- Statistical Scoring

---

## 📁 PROJECT STRUCTURE

Project---RFM-Segmentation/
├── README.md
├── BUSINESS_INSIGHTS.md         (deep-dive findings — see link above)
├── LICENSE
├── requirements.txt
├── Data/
│   ├── rfm_segments.csv          (4,312 customers with RFM scores)
│   ├── clv_segments.csv          (CLV calculated for 2,815 repeat customers — see Methodology)
│   └── cohort_matrix.csv         (retention data)
├── Notebook/
│   └── customer_analytics.ipynb  (full Python analysis, step by step)
├── Dashboard/
│   └── RFM-Dashboard.pbix        (all 3 report pages in one file)
└── Visuals/
    ├── RFM Customer Segmentation Analysis.png
    ├── Customer Lifetime Value Analysis.png
    └── Customer Retention Analysis.png

---

## 💼 TECHNICAL SKILLS DEMONSTRATED

✅ **Data Analysis**
- RFM segmentation methodology
- Customer Lifetime Value calculation
- Cohort analysis & retention tracking
- Statistical analysis & scoring

✅ **Data Visualization**
- Power BI dashboard creation
- Multiple chart types (bar, line, scatter, heatmap)
- Interactive filtering with slicers
- Professional design and formatting

✅ **Business Analysis**
- Customer segmentation strategy
- Retention pattern identification
- Value tier analysis
- Cohort behavior analysis

---

## 🎓 KEY TAKEAWAYS

**What the data shows about this business:**

1. **Customer Concentration:** 21% of customers generate 65% of revenue
2. **Retention Challenge:** 85% of new customers don't become repeat buyers
3. **Value Growth:** Customers who stay long-term become 17x more valuable
4. **Segmentation Works:** RFM framework accurately identifies customer tiers
5. **Engagement Matters:** Different customer segments behave very differently

---

## 📊 BUSINESS METRICS

| Metric                        | Value    |
|--------------------------------|----------|
| Total Customers                | 4,312    |
| Total Orders                   | 19,213   |
| Total Revenue                  | £8,832,003 |
| Customers with CLV calculated* | 2,815    |
| Total CLV (of the 2,815)       | £78.25M  |
| Average CLV (of the 2,815)     | £27.80K  |
| Average Order Value            | £459.69  |
| Revenue per Customer           | £2,048.24  |
| Champion Customers             | 926 (21%) |
| New Customers                  | 1,358 (32%) |
| Average Retention Rate         | 35%      |

*CLV excludes ~1,500 one-time buyers whose first and last purchase fall on the
same day — the CLV formula naturally returns 0 for them. See Methodology.

---

## 🎯 INTERVIEW TALKING POINTS

**Project Summary (60 seconds):**
"I analyzed 4,312 customers using RFM segmentation and lifetime value analysis. The analysis shows clear customer tiers: Champions (21% of base) generate 65% of revenue with an average CLV of £35K, while New customers (32% of base) have only £2K CLV. Retention data reveals that 85% of new customers churn by month 12, with only 35% average retention across cohorts. RFM scores successfully predict customer value - high scores correlate with high CLV. The key insight is that customers who stay longer become increasingly valuable, with Champions spending 17x more than new customers."

---

## 👤 ABOUT THIS ANALYSIS

**Analyst:** Priyanshu  
**Data Source:** Online Retail II Dataset  
**Analysis Period:** 2009-2010  
**Methodology:** RFM Segmentation + CLV Analysis  
**Tools:** Python, Power BI  
**Status:** Completed and ready for review

---

**This project demonstrates how to take transaction data and create actionable customer insights through segmentation analysis.**

