# PISA Loan Data Exploration
## by Adiji Ayomiposi


## Dataset

This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.

But the features I wil base my analysis on are:

- **ListingCreationDate**: The date the listing(request for the loan) was created.

- **BorrowerAPR**: The Borrower's Annual Percentage Rate (APR) for the loan.

- **ProsperRating (Alpha)**: The Prosper Rating assigned at the time the listing was created between AA - HR. Applicable for loans originated after July 2009.

- **ProsperScore**: A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score.  Applicable for loans originated after July 2009.

- **ListingCategory (numeric)**: The category of the listing that the borrower selected when posting their listing: 0 - Not Available, 1 - Debt Consolidation, 2 - Home Improvement, 3 - Business, 4 - Personal Loan, 5 - Student Use, 6 - Auto, 7- Other, 8 - Baby&Adoption, 9 - Boat, 10 - Cosmetic Procedure, 11 - Engagement Ring, 12 - Green Loans, 13 - Household Expenses, 14 - Large Purchases, 15 - Medical/Dental, 16 - Motorcycle, 17 - RV, 18 - Taxes, 19 - Vacation, 20 - Wedding Loans

- **Occupation**: The Occupation selected by the Borrower at the time they created the listing.

- **IsBorrowerHomeowner**: A Borrower will be classified as a homowner if they have a mortgage on their credit profile or provide documentation confirming they are a homeowner.

- **CreditScoreRangeLower**: The lower value representing the range of the borrower's credit score as provided by a consumer credit rating agency.

- **CreditScoreRangeUpper**: The upper value representing the range of the borrower's credit score as provided by a consumer credit rating agency. 

- **DebtToIncomeRatio**: The debt to income ratio of the borrower at the time the credit profile was pulled. This value is Null if the debt to income ratio is not available. This value is capped at 10.01 (any debt to income ratio larger than 1000% will be returned as 1001%).

- **IncomeRange**: The yearly income range of the borrower at the time the listing was created.

- **IncomeVerifiable**: The borrower indicated they have the required documentation to support their income.

- **StatedMonthlyIncome**: The monthly income the borrower stated at the time the listing was created.

- **LoanMonthsSinceOrigination**: Number of months since the loan originated.

- **LoanOriginalAmount**: The origination amount of the loan.

- **MonthlyLoanPayment**: The scheduled monthly loan payment.

- **Investors**: The number of investors that funded the loan.

After series of little data wrangling

There are 76,168 reords of people in the dataset with 14 features. Most variables are numeric in nature, but the variables ProsperRating (Alpha) and IncomeRange are ordered factor variables with the following levels.

(least) ——> (best) <br>
ProsperRating (Alpha): HR, E, D, C, B, A, AA <br>
IncomeRange: Not employed, $1-24,999, $25,000-49,999, $50,000-74,999, $75,000-99,999, $100,000+

Is Borrower Homeowner is boolean datatype

The Listing category and occupation are unordered category types

The Listing Creation Date is in datetime datatype

## Summary of Findings

I found out that the Loan features(amount and monthly payment) were greatly correlated with the Borrower Rate.

The home owner feature also gave very clear relationship with the Borrower Rate.

The Employment features like occupation, income range and the monthly income also were very good at describing the dataset.

As the times go by the annual rating also seems to drop something to keep an eye for.


## Key Insights for Presentation

I will be focusing on the home owner feature, Loan amount and the Income status( Income Range, employment) as the relate with the Annual Borrower Rate.