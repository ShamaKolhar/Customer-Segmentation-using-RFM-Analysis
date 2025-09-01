#### Customer Segmentation using RFM Analysis
### Overview

This project performs RFM (Recency, Frequency, Monetary) analysis on e-commerce transaction data to segment customers into actionable groups such as Champions, Potential Loyalists, and At Risk customers.

RFM is a powerful technique in marketing analytics to understand customer behavior and prioritize retention or growth strategies.

### Dataset
This project uses the online retail dataset from Kaggle - (https://www.kaggle.com/datasets/vijayuv/onlineretail).
### Project Workflow

## Data Cleaning & Preparation

Converted dates to datetime format.

Removed null customer IDs and negative transactions (returns).

Created an Amount = Quantity × UnitPrice column.

Aggregated to order-level transactions.

## RFM Calculation

Recency: Days since last purchase.

Frequency: Number of unique purchases.

Monetary: Total spend.

## Scoring & Segmentation

Scored R, F, M into quintiles (1–5) using pd.qcut.

Combined into RFM_Segment (e.g., 543).

Summed into RFM_Score (range 3–15).

Mapped customers into business segments:

Champions (high R, F, M)

Potential Loyalists

At Risk / Lost

## Visualization & Insights

Histograms for Recency, Frequency, and Monetary distributions.

Log transformation for skewed Monetary distribution.

Bar charts of customer segments with counts and percentages.

### Insights

Majority of customers are low-frequency, low-spend buyers.

A small set of Champions ( almost top 10–15%) contribute disproportionately to revenue.

Many customers fall into the Potential group, an opportunity for targeted campaigns.

At Risk customers (long recency, previously high frequency) need re-engagement strategies.

### Project Structure
RFM-Analysis/
│── data/                 # raw and processed datasets
│── notebooks/            # main analysis notebook
│── outputs/              # plots and RFM segment results
│── README.md             # project documentation

Author : Shama Kolhar
