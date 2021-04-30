# Udacity Advanced Data Analysis: Data Visualization & Communication Project

# Prosper Loans Data Exploration

This project has two parts that demonstrate the importance and value of data visualization techniques in the data analysis process.
In the first part, I use Python visualization libraries to systematically explore the Prosper Loans dataset, starting from plots of single variables and building up to plots of multiple variables.

In the second part, I made a short presentation that illustrates interesting properties, trends, and relationships I discovered.

## Dataset

The Prosper Loans dataset has details about 113,937 loans with 81 attributes related with those loans.

> I Chose to work with 17 of those attributes, namely, ('ListingNumber', 'LoanOriginalAmount', 'Term', 'LoanStatus', 'BorrowerAPR', 'BorrowerRate', 'ListingCategory (numeric)', 'BorrowerState', 'Occupation', 'EmploymentStatus', 'IsBorrowerHomeowner', 'AmountDelinquent', 'AvailableBankcardCredit', 'DebtToIncomeRatio', 'StatedMonthlyIncome', 'Recommendations').

> Most of those attributes are numeric, but the variables ('LoanStatus', 'ListingCategory (numeric)', 'BorrowerState', 'Occupation', 'EmploymentStatus', 'IsBorrowerHomeowner') are categorical nominal variables.

## Files

-   `exploration.ipynb`: the main code and report for the data analysis & visualization efforts.
-   `exploration.html`: the exported HTML file of the jupyter notebook.
-   `slide_deck.ipynb`: the main code for the final slides.
-   `slide_deck.slides.html`: the exported HTML file of the slides.
-   `prosperLoanData.csv`: the original Prosper Loan dataset.
-   `Prosper Loan Data - Variable Definitions.xlsx`: an additional file that explains the Prosper dataset variables.
-   `output_toggle.tpl`: this template file can be used with nbconvert to export your slide deck it adds extra functionality to the slide deck by hiding the code to start, only making it visible if the reader clicks on the output (which should mostly be visualizations in the case of this project). find the original [here](https://github.com/damianavila/blog/blob/master/posts/hide-the-input-cells-from-your-ipython-slides.ipynb)

## Summary of Findings

-   Most common Loan Statuses are Current, Completed, Chargedoff, and Defaulted, respectively.
-   California is the state with the highest number of Loans.
-   The most common listing for the loans is Debt Consolidation.
-   The most common Loan Term is 30 months, followed by 60 months, and then 12 months.
-   Most of the variable didn't have the effect I initially assumed they would have on the Loan Status. Surprisingly enough, variables like the Debt to Income Ratio and the Loan Original Amount didn't have much impact on whether a Loan was Completed or not.
-   Completed Loans seem to correlate with a slightly higher Monthly Income than that of Defaulted.
-   Another surbrusing result was that homeowners didn't complete loans more than those who are not homeowners.
-   There is a negative correlation between the Debt to Income Ratio and the Monthly Income, which is natural.
-   There is also some level of positive correlation between the Monthyly Income and the Original Loan Amount. As one of them increases, so does the other.
-   A surprising finding is that there is a level of negatice correlation between Original Loan Amount and the Borrower APR.
-   Borrower APR does in fact affect the Loan Status (In a given Loan Term, APR tends to inversely correlate with the Loan Status). Furthermore, it appears a longer Loan Term leads to Completed or Current Loan Status with higher APR values.
-   For a 12 month Loan Term, any APR higher than 0.22 would lead to Default, Chargeoff, or payment delay.
-   For a 36 month Loan Term, any APR higher than 0.237 would lead to Default, Chargeoff, or payment delay.
-   For a 60 month Loan Term, any APR higher than 0.238 would lead to Default, Chargeoff, or payment delay.

## Key Insights for Presentation

For the presentation I focus on Loan Term and the Borrower's Annual Percentage Rate and their effect on the Loan Status.

## Requirements

-   [Pandas](https://pandas.pydata.org/)
-   [NumPy](https://numpy.org/)
-   [Matplotlib](https://matplotlib.org/)
-   [Seaborn](https://seaborn.pydata.org/)

## Resources used

-   [Dataframe Reindexing](https://stackoverflow.com/questions/28885073/reindexing-after-pandas-drop-duplicates)
-   [Understanding APR & Interest Rate](https://www.bankofamerica.com/mortgage/learn/apr-vs-interest-rate/)
