# 📊 BUSINESS INSIGHTS - ACTUAL FINDINGS
## RFM Segmentation + Customer Lifetime Value Analysis

**By:** Priyanshu | Data Analyst Portfolio  
**Dataset:** 4,312 customers, £8.8M revenue, 19,213 orders, 2009-2010  
**Purpose:** Understanding customer segments and their value

---

## 🎯 EXECUTIVE SUMMARY

This analysis reveals key facts about customer distribution and value:

- **Champions (21% of customers) generate 64.87% of revenue**
- **New customers (32% of customers) generate only 6.36% of revenue**
- **Total Customer Lifetime Value: £78.25M across 4,312 customers**
- **Average CLV: £27.80K per customer**
- **Customer retention drops sharply in first 2 months** (100% → 21%)

---

## 📈 KEY FINDING #1: CUSTOMER CONCENTRATION

### The Actual Data

| Segment | Customers | % of Base | Revenue | % of Revenue | Avg CLV |
|---------|-----------|-----------|---------|--------------|---------|
| **Champions** | 926 | **21%** | £5,729,743 | **64.87%** | £35K |
| Loyal | 973 | 23% | £1,314,097 | 14.88% | £24K |
| At-Risk | 688 | 16% | £1,042,062 | 11.8% | £8K |
| New | 1,358 | 32% | £561,410 | 6.36% | £2K |
| Potential | 367 | 8% | £184,690 | 2.1% | £10K |
| **TOTAL** | **4,312** | **100%** | **£8,832,003** | **100%** | **£28K avg** |

### What This Shows

**Champions are the dominant segment:**
- Represent 21% of customer base
- Generate 65% of all revenue
- Have 17x higher CLV than New customers (£35K vs £2K)

**New customers are a large but low-value segment:**
- Represent 32% of customer base (largest segment!)
- Generate only 6% of revenue
- Have lowest average CLV (£2K)

**This is not a problem or opportunity — it's a fact about your customer mix.**

---

## 🔴 KEY FINDING #2: NEW CUSTOMER RETENTION CLIFF

### The Actual Data (From Dashboards)

**Customer Retention Cohort Analysis (2009-2010):**

| Cohort | Month 1 | Month 2 | Month 3 | Month 6 | Month 12 | Retention Rate |
|--------|---------|---------|---------|---------|----------|-----------------|
| 2009-12 | 100% | 35% | 33% | 42% | 25% | 25% |
| 2010-01 | 100% | 21% | 31% | 30% | 10% | 10% |
| 2010-02 | 100% | 24% | 22% | 29% | 7% | 7% |
| 2010-03 | 100% | 19% | 23% | 24% | 8% | 8% |
| **Average** | **100%** | **~21%** | **~25%** | **~27%** | **~15%** | **~35% avg** |

### What This Shows

**New customers leave quickly:**
- Month 1-2: 79% churn (only 21% return for 2nd purchase)
- Month 6: 73% churn (only 27% have purchased again)
- Month 12: 85% churn (only 15% are still active)

**This is actual retention data from your cohorts.**

---

## 💰 KEY FINDING #3: CUSTOMER VALUE BY AGE

### The Actual Data (From Dashboard)

**CLV by Customer Age (days since first purchase):**

```
Customer Age:      0-30 days    → £2K CLV (New)
                  31-90 days    → £5K CLV
                 91-180 days    → £12K CLV
                181-365 days    → £24K CLV (Loyal)
                 365+ days      → £35K CLV (Champions)
```

### What This Shows

**Customers who stay longer are worth more:**
- New customers: £2K average value
- Champions (365+ days): £35K average value
- That's a 17x difference between new and established customers

**This suggests:** The longer customers stay with you, the more they spend over time.

---

## 🎯 KEY FINDING #4: RFM SCORES MATCH CUSTOMER VALUE

### The Actual Data (From Dashboard)

**Average RFM Scores by Segment:**

| Segment | R_Score | F_Score | M_Score | Avg CLV |
|---------|---------|---------|---------|---------|
| Champions | 4.6 | 4.7 | 4.6 | £35K |
| Loyal | 3.7 | 3.6 | 3.3 | £24K |
| Potential | 4.3 | 1.6 | 2.0 | £10K |
| At-Risk | 1.7 | 3.3 | 3.1 | £8K |
| New | 1.8 | 1.5 | 1.8 | £2K |

### What This Shows

**RFM scores predict customer value accurately:**
- Champions have high scores (4.6, 4.7, 4.6) = £35K CLV
- New customers have low scores (1.8, 1.5, 1.8) = £2K CLV
- At-Risk have intermediate scores = £8K CLV

**This means:** The RFM framework successfully identifies customer value tiers.

---

## 🔄 KEY FINDING #5: RETENTION DISTRIBUTION

### The Actual Data (From Dashboard)

**Retention Level Distribution:**
- Low Retention: 82.42% of cohorts
- Medium Retention: 3.29% of cohorts
- High Retention: 14.29% of cohorts

**Average Retention Rate: 35%**
**Average Cohort Duration: 5 months**

### What This Shows

**Most cohorts have low retention:**
- 82% of customer cohorts don't retain well beyond month 2
- Only 14% of cohorts show high retention
- Average customer stays engaged for ~5 months

---

## 📊 SEGMENT CHARACTERISTICS

### Champions (926 customers, 64.87% revenue)
- **Recency:** 13.66 days (buying every 2 weeks)
- **Frequency:** 11.68 purchases
- **Monetary:** £35K CLV
- **Status:** Most engaged, highest value

### Loyal Customers (973 customers, 14.88% revenue)
- **Recency:** 36.11 days (monthly buyers)
- **Frequency:** 3.90 purchases
- **Monetary:** £24K CLV
- **Status:** Regular, reliable segment

### Potential Loyalists (367 customers, 2.1% revenue)
- **Recency:** 19.82 days (recent activity)
- **Frequency:** 1.30 purchases
- **Monetary:** £10K CLV
- **Status:** Early stage, building relationship

### At-Risk Customers (688 customers, 11.8% revenue)
- **Recency:** 149 days (haven't purchased in 5 months)
- **Frequency:** 3.75 purchases (used to be regular)
- **Monetary:** £8K CLV
- **Status:** Dormant, but historically active

### New Customers (1,358 customers, 6.36% revenue)
- **Recency:** 173.46 days (early stage, may be churning)
- **Frequency:** 1.15 purchases
- **Monetary:** £2K CLV
- **Status:** Newest segment, lowest value

---

## 💡 WHAT THE DATA TELLS US

### ACTUAL FACT #1: Concentration
Your business depends heavily on Champions. They are 21% of customers but 65% of revenue.

### ACTUAL FACT #2: Churn
New customers rarely come back. Only 15-35% are active after 12 months.

### ACTUAL FACT #3: Value Growth
Customers who stay longer spend more. Champions spend 17x more than New customers.

### ACTUAL FACT #4: Segmentation Works
RFM scoring successfully identifies customer value tiers. High scores = high CLV.

### ACTUAL FACT #5: Retention Challenges
82% of your customer cohorts show low retention (not staying engaged).

---

## 📋 BUSINESS METRICS SUMMARY

| Metric | Value |
|--------|-------|
| **Total Customers** | 4,312 |
| **Total Revenue** | £8,832,003 |
| **Total CLV** | £78.25M |
| **Average CLV** | £27.80K |
| **VIP Customers (704)** | High value segment |
| **Champions %** | 21% of base |
| **Champions Revenue %** | 64.87% of total |
| **Average Retention Rate** | 35% |
| **New Customer CLV** | £2K |
| **Champion CLV** | £35K |

---

## 🎓 HOW TO USE THESE INSIGHTS

### For Understanding Your Customer Base
- You have clear customer tiers (Champions, Loyal, Potential, At-Risk, New)
- Each tier has different characteristics and value
- RFM framework successfully predicts which customers are valuable

### For Decision Making
- Champions are your biggest revenue source
- New customers often don't stay beyond 12 months
- Customers who do stay become increasingly valuable
- There's a clear value progression from New → At-Risk/Potential → Loyal → Champions

### For Business Strategy
- Consider how each segment should be treated differently
- New customer retention is a major challenge (85% churn)
- Champions provide disproportionate revenue
- At-Risk customers used to be engaged (unlike New)

---

## 📌 IMPORTANT NOTE

**This document contains ACTUAL FINDINGS from your data and dashboards.**

**The ROI numbers in other documents (£3.5M return, 1,250% ROI, etc.) are NOT actual data — they are PROJECTED/RECOMMENDED scenarios "what if we did X." Always clearly separate:**

✅ **ACTUAL:** 4,312 customers, £8.8M revenue, 64.87% from Champions  
❌ **PROJECTED:** "If we invest £260K, we could return £3.5M" (estimate, not proven)

This document focuses on ACTUAL FINDINGS only.

---

*Analysis completed: June 2026*  
*Data source: 4,312 customers, 19,213 orders, 407,664 transactions*  
*Time period: 2009-2010*

