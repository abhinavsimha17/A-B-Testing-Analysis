# A/B Test Analysis: Which Website Version Sells More?

An online store tested its current website (**Control**) against two new versions (**Variant A** and **Variant B**). This project uses 2 million user actions and 103K purchases to find out which version works best.



## Dataset

This project uses the [Marketing and E-commerce Analytics Dataset](https://www.kaggle.com/datasets/geethasagarbonthu/marketing-and-e-commerce-analytics-dataset/data) from Kaggle. It includes website events, transactions, customers, products and campaigns.

## Results

| | Control | Variant A | Variant B |
|---|---|---|---|
| Purchase rate | 4.74% | 5.24% | **6.30%** |
| Improvement over Control | – | +10.5% | **+32.9%** |
| Revenue per visit | $3.90 | $4.28 | **$5.07** |

**Variant B is the winner.** It increased purchases by 33% and revenue by 30%. It also worked on every device and traffic source, and it didn't cause more people to leave the site or ask for refunds.

## What I did

1. **Cleaned the data:** fixed inconsistent labels, filled missing values, and linked purchases to revenue.
2. **Checked the test was fair:** each group got the right share of traffic, and the groups had the same mix of devices and traffic sources.
3. **Compared the groups:** used statistical tests to confirm the differences were real and not due to chance.
4. **Looked at segments:** checked the results by device and traffic source.
5. **Checked the test size:** the sample was large enough to spot even small changes.


## Limitations

- The same customer could see more than one version of the site. A follow-up test that keeps each customer in one group would confirm the result.
- About 10% of purchases had no revenue value, so they were left out of the revenue numbers.

## Tools

Python, pandas, NumPy, SciPy, statsmodels, matplotlib, Jupyter

## How to run

1. Download the dataset from Kaggle and put the CSV files in the `data/` folder.
2. Install the libraries: `pip install -r requirements.txt`
3. Open `notebooks/ab_test_analysis.ipynb` and run all cells.
