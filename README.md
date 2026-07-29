# Business-Intelligence-
# Retail Profitability Analysis and Decision-Tree Modelling

**First-Class Business Intelligence Project | 2026**

## Project overview

This individual project investigated how discounting, product mix, location and sales performance influence retail profitability.

I analysed **9,994 transactions** from the US Superstore dataset, which contains information about sales, profit, discounts, products, customer segments, shipping methods and geographic regions.

The project addressed the following business question:

> How do discounting behaviour, product mix and sales performance influence profitability, and how can these relationships support better pricing, category and regional decisions?

I combined visual analysis in **Tableau** with decision-tree modelling in **WEKA Explorer** to identify business patterns and develop practical recommendations.

## What I did

- Examined the dataset for missing values, duplicates, inconsistent data types and irrelevant identifiers.
- Created **10 Tableau visualisations** covering sales, profit, discounts, customer segments, regional performance and seasonal demand.
- Compared business performance across categories, sub-categories, cities, regions and customer segments.
- Used Tableau forecasting to investigate sales trends and recurring seasonal patterns.
- Prepared the dataset for modelling by removing non-analytical identifiers and less informative attributes.
- Converted numerical profit values into three classification outcomes: **High Profit, Low Profit and Loss**.
- Built three versions of a **J48 decision-tree classifier** in WEKA Explorer.
- Compared the models based on accuracy, complexity, interpretability and usefulness for business decision-making.
- Translated the findings into recommendations for pricing, inventory planning, category prioritisation and regional strategy.

## Tableau findings

The visual analysis identified several important patterns:

- **Technology** generated the strongest sales and profit performance.
- **Furniture** produced weaker profitability despite generating substantial sales.
- Sales were concentrated in the **West and East regions**.
- The Consumer segment contributed the largest share of sales across regions.
- Some high-revenue sub-categories produced relatively weak profits, demonstrating that sales volume alone did not guarantee profitability.
- Sales followed a recurring seasonal pattern, with stronger performance in **Q4** and predictable declines during **Q1**.
- Higher discounts were consistently associated with weaker profit margins and loss-making transactions.

## Decision-tree modelling

I selected the **J48 decision-tree algorithm** because it can analyse numerical and categorical variables while producing transparent if-then rules that business users can interpret.

The model classified transactions into High Profit, Low Profit or Loss outcomes. I tested three different combinations of attributes to balance predictive performance with model simplicity.

| Model | Attributes | Accuracy | Tree size | Assessment |
|---|---:|---:|---:|---|
| Iteration 1 | 9 | 95.46% | 260 nodes | Highest accuracy but overly complex |
| Iteration 2 | 7 | 93.06% | 45 nodes | Best balance of accuracy and interpretability |
| Iteration 3 | 5 | 92.84% | 33 nodes | Simplest model but reduced regional insight |

I selected **Iteration 2** as the most useful model. It retained important regional information while reducing the tree from 260 to 45 nodes and maintaining **93.06% training accuracy**.

## Key model finding

Discount was the most influential variable in the decision tree.

Transactions with discounts above **20%** were substantially more likely to be classified as loss-making. This pattern remained consistent across all three model iterations and supported the findings from the Tableau analysis.

## Business recommendations

Based on the combined analysis, I recommended:

- Introducing stronger controls and approval rules for discounts above 20%.
- Reviewing combinations of categories, customer segments and discount levels associated with losses.
- Evaluating product performance using both sales and profit instead of revenue alone.
- Adapting marketing and resource allocation to regional performance.
- Planning inventory and operational capacity around predictable Q4 demand.
- Using interpretable decision rules to support pricing and profitability decisions.

## Tools and techniques

- Tableau
- WEKA Explorer
- J48 decision-tree classification
- Data cleaning and preprocessing
- Attribute selection
- Data visualisation and forecasting
- Model comparison and interpretation
- Business analysis
- Evidence-based recommendations

## Result

This project received a **First-Class grade**.

## Limitations

The decision-tree models were evaluated using the training dataset rather than cross-validation or a separate test set. Therefore, the reported accuracy measures performance on the available data and may overestimate performance on unseen transactions.

A future version of the project would use stratified cross-validation or a held-out test set to evaluate how well the model generalises to new transactions.
