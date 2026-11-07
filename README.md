# Cognifyz Business Analytics Internship

**Author:** Aziz Chharchhoda
**Program:** Business Analytics Internship, Cognifyz IT Solutions Pvt. Ltd. (Oct - Nov 2026)

## About

This project analyses an investment-preference survey of 40 respondents (24 columns). It covers 10 tasks across 4 levels, from basic data overview to correlation analysis. Each task has its own notebook.

## Project structure

```
cognifyz-business-analytics-internship/
├── README.md
├── requirements.txt
├── data/
│   └── Data_set_2.csv
├── notebooks/
│   ├── level1_task01_data_overview.ipynb
│   ├── level1_task02_gender_distribution.ipynb
│   ├── level2_task03_descriptive_statistics.ipynb
│   ├── level2_task04_preferred_investment_avenue.ipynb
│   ├── level3_task05_reasons_for_investment.ipynb
│   ├── level3_task06_savings_objectives.ipynb
│   ├── level4_task07_information_sources.ipynb
│   ├── level4_task08_investment_duration.ipynb
│   ├── level4_task09_investment_expectations.ipynb
│   └── level4_task10_correlation_analysis.ipynb
└── outputs/
    └── charts/
```

## Tools used

Python, pandas, NumPy, matplotlib, seaborn, SciPy, Jupyter (VS Code)

## How to run

```
pip install -r requirements.txt
```

Open any notebook in `notebooks/` and run all cells. Each notebook reads the data from `../data/Data_set_2.csv`, and charts are saved to `outputs/charts/`.

## Key findings

**Task 1 - Data overview**
The dataset has 40 rows and 24 columns, with no missing values and no duplicate rows. Only `age` is a true numeric column. The seven investment columns (Mutual Funds, Equity, Debentures, Government Bonds, Fixed Deposits, PPF, Gold) are preference ranks from 1 to 7, where 1 is the most preferred.

**Task 2 - Gender distribution**
25 respondents are male (62.5%) and 15 are female (37.5%).

**Task 3 - Descriptive statistics**
Age: mean 27.8, median 27, standard deviation 3.56, range 21 to 35. Average preference rank (lower is more preferred): PPF 2.02, Mutual Funds 2.55, Equity 3.48, Fixed Deposits 3.58, Government Bonds 4.65, Debentures 5.75, Gold 5.98.

**Task 4 - Most preferred investment avenue**
Mutual Funds is the most chosen avenue (18 of 40, 45%), followed by Equity (10, 25%), Fixed Deposits (9, 22.5%) and PPF (3, 7.5%). One inconsistency: PPF has the best average rank but is chosen as the main avenue by only 3 people, so the ranking question and the avenue question do not fully agree.

**Task 5 - Reasons for investment**
- Equity: Capital Appreciation (30 of 40)
- Mutual Funds: Better Returns (24), Fund Diversification (13)
- Bonds: Assured Returns (26), Safe Investment (13)
- Fixed Deposits: Risk Free (19), Fixed Returns (18)

Returns drive the choice for equity and mutual funds, while safety drives the choice for bonds and fixed deposits.

**Task 6 - Savings objectives**
Retirement Plan is the main objective (24, 60%), then Health Care (13, 32.5%) and Education (3, 7.5%).

**Task 7 - Information sources**
Financial Consultants (16, 40%) and Newspapers and Magazines (14, 35%) are the top sources. Television follows with 6 (15%), and the Internet is the least used with 4 (10%).

**Task 8 - Investment duration**
Most respondents plan to invest for 1 to 5 years (37 of 40). Duration was given as ranges, so I converted them to midpoints (less than 1 year = 0.5, 1-3 = 2, 3-5 = 4, more than 5 = 6). The average duration is about 3 years.

**Task 9 - Expectations from investments**
32 of 40 respondents (80%) expect returns of 20% to 30%, 5 expect 30% to 40%, and 3 expect 10% to 20%. These expectations are high compared with what fixed deposits, PPF and bonds usually pay.

**Task 10 - Correlation analysis**
Using Spearman correlation on age, investment duration and expected return (the last two converted to numbers as above):
- Age and duration: 0.04 (p = 0.79)
- Age and expected return: -0.10 (p = 0.53)
- Duration and expected return: 0.26 (p = 0.11)

None of these is statistically significant at the 5% level. There is a weak hint that people planning longer durations expect higher returns, but the sample is too small to confirm it.

## Limitations

- The sample is small (40 respondents), so the findings describe this group only and should not be generalised.
- Duration and expected return were given as ranges. Converting them to midpoints is an assumption and affects the averages and correlations.
- Preference ranks are ordinal, so averages of ranks should be read as "average position", not as quantities.