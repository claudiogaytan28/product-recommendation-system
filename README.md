# Product Recommendation System from Retail Transactions

A product recommendation system built from retail transaction data using
market basket analysis, identifying which products are frequently
purchased together and generating ranked recommendations for any given
product.

## Problem

Retailers often miss opportunities to increase basket size by failing to
suggest relevant products at the right moment. This project answers a
practical question: **given a product a customer is buying, what other
products should be recommended to them?**

## Approach

1. Data cleaning and transaction-level preparation
2. Exploratory analysis of basket size and product frequency
3. Market basket analysis using the Apriori algorithm
4. Association rule mining (support, confidence, lift)
5. Rule stability validation across multiple random samples
6. Recommendation function: given a product, return its top related items

## Key findings

- **Limited natural co-purchase structure:** product frequencies are
  nearly uniform across the catalog (~36,000–37,000 occurrences each), and
  the strongest association rules found had a lift of only ~1.16 — close to
  the threshold that indicates no relationship at all.
- **Patterns are stable, even if weak:** re-running the analysis on 5
  independent random samples produced largely the same top rules each time,
  confirming the relationships found are consistent rather than random noise.
- **Methodology is sound and transferable:** the recommendation function
  works as designed. In a business setting with genuine co-purchase
  patterns, this same pipeline would be expected to surface significantly
  stronger and more actionable recommendations.

## Tools

Python · pandas · mlxtend · scikit-learn · matplotlib · seaborn

## Notebook

[View full notebook →](./02_product_recommendation_system.ipynb)
