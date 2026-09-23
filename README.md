# Banking-Customer-Exploratory-Data-Analysis
Exploratory Data Analysis of a 3,000-customer banking dataset uncovering correlations in deposits, loans, income, and customer loyalty.

## Project Overview

This project performs a comprehensive **Exploratory Data Analysis (EDA)** on a banking customer dataset containing **3,000 clients** and **25 features**. The goal is to uncover patterns in customer demographics, account balances, lending behavior, loyalty tiers, and risk profiles to support data-driven banking decisions (cross-selling, risk assessment, customer segmentation, etc.).

The analysis focuses on relationships between deposit accounts, loans, income, age, and other financial metrics using statistical summaries, correlation analysis, and visualization techniques.

## Dataset

**File:** `Banking.csv`  
**Size:** 3,000 rows × 25 columns  
**No missing values**

### Key Features

| Category              | Columns |
|-----------------------|---------|
| **Demographics**      | Client ID, Name, Age, Nationality, GenderId, Occupation, Location ID, Joined Bank |
| **Banking Relationship** | Banking Contact, Fee Structure, Loyalty Classification, Risk Weighting, BRId, IAId |
| **Financial Products** | Estimated Income, Superannuation Savings, Amount of Credit Cards, Credit Card Balance, Bank Loans, Bank Deposits, Checking Accounts, Saving Accounts, Foreign Currency Account, Business Lending, Properties Owned |

### Snapshot of Data Distribution
- **Age**: Mean ≈ 51 years (range 17–85)
- **Nationality**: European (43.6%), Asian (25.1%), American (16.9%), Australian (8.5%), African (5.9%)
- **Loyalty Classification**: Jade (44.4%), Silver (25.6%), Gold (19.5%), Platinum (10.6%)
- **Fee Structure**: High (49.2%), Mid (32.1%), Low (18.7%)

## Key Insights from EDA

### 1. Strong Positive Correlations Among Deposit Accounts
- **Bank Deposits** shows the strongest relationships with:
  - Checking Accounts (r ≈ 0.84)
  - Saving Accounts (r ≈ 0.75)
  - Foreign Currency Account (r ≈ 0.41)
- Customers who maintain high balances in one account type tend to hold substantial funds across multiple account types.

### 2. Income, Age & Wealth Accumulation
- Estimated Income is moderately correlated with Superannuation Savings, Bank Loans, Business Lending, and various deposit balances.
- Older customers and higher-income individuals generally show higher savings, retirement balances, and credit utilization — consistent with typical financial lifecycle patterns.

### 3. Lending Behavior
- **Business Lending** has a moderate positive correlation with Bank Loans (r ≈ 0.42), indicating some customers carry both personal and business debt.
- Business lending is relatively independent of pure deposit metrics, suggesting it serves a distinct customer segment.

### 4. Property Ownership
- Properties Owned shows very weak correlations with most banking variables, implying that real-estate decisions are driven by external factors (location, market conditions, inheritance, etc.) not fully captured in this dataset.

### 5. Visual Relationships (Regression Plots)
Scatter plots with regression lines were generated for key pairs, including:
- Bank Deposits vs Saving Accounts
- Checking Accounts vs Saving Accounts
- Checking Accounts vs Foreign Currency Account
- Age vs Superannuation Savings
- Estimated Income vs Checking Accounts
- Bank Loans vs Credit Card Balance
- Business Lending vs Bank Loans

These visualizations confirm the correlation findings and highlight linear trends and outliers.

## Tools & Libraries Used

- **Python 3**
- **pandas** – data loading, cleaning, and summary statistics
- **numpy** – numerical operations
- **matplotlib** & **seaborn** – statistical visualizations and regression plots
- **Jupyter Notebook** – interactive analysis environment
