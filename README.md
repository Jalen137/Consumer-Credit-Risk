# Consumer-Credit-Risk

Estimating the chance that someone will not pay back their loan. Then I will take this information and decide whether to give them the loan or not. 

## Business Question
How do we decide which applicants to approve for credit while mitigating the default losses and maximizing our companies profit? 

## Project Overview
This project's purpose is to build a credit risk model to estimate the probability of default for loan applicants and uses that risk to make approval decisions that balance the profit in the loss from the loans. 

## Mock company 
This analysis is framed around a mock medium-sized consumer lending company that gives out personal loans. The company wants to grow revenue while controlling default losses. 

## Dataset

### Where it comes from
Got it from the UC Irvine Machine Learning Repository  
https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients

### What it represents
This dataset represents real consumer credit card behavior, including credit limits, repayment history, billing amounts, and past payment behavior. Each observation corresponds to a single borrower and whether they defaulted on their payment in the following month.

### Why I chose it
I chose this dataset because it closely mirrors how real lenders evaluate risk. It contains behavioral data, not just demographics, which makes it useful for modeling default risk and building real approval rules rather than just making predictions.

### Dataset Discription
This research employed a binary variable, default payment (Yes = 1, No = 0), as the response variable. This study reviewed the literature and used the following 23 variables as explanatory variables:

- **X1:** Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit.  
- **X2:** Gender (1 = male; 2 = female).  
- **X3:** Education (1 = graduate school; 2 = university; 3 = high school; 4 = others).  
- **X4:** Marital status (1 = married; 2 = single; 3 = others).  
- **X5:** Age (year).  
- **X6–X11:** History of past payment from April to September 2005.  
  - -1 = pay duly  
  - 1 = payment delay for one month  
  - 2 = payment delay for two months  
  - …  
  - 9 = payment delay for nine months and above  
- **X12–X17:** Amount of bill statement (NT dollar) from April to September 2005.  
- **X18–X23:** Amount of previous payment (NT dollar) from April to September 2005.  

## How I went about the project
- Look for a good dataset  
- Data cleaning and fixing data types  
- Feature grouping based on borrower behavior, capacity, and demographics  
- Default prediction models  
- Risk-based approval rules tied to profit and loss  

## Models Used
Two models were built and compared:

- **Logistic Regression**  
  Used as a baseline model because it is simple and interpretable.

- **XGBoost**  
  Used as an improved model to capture non-linear relationships in the data.

Both models were evaluated using the same train-test split and decision framework.

## Decision Framework
Applicants are segmented into Low, Medium, and High Risk bands based on predicted default probability percentiles. Approval decisions are driven by expected profit, with High Risk applicants rejected due to large expected losses, while Low and Medium Risk applicants are approved or reviewed.

## Evaluation Metrics
- ROC-AUC to measure how well the model separates defaulters from non-defaulters  
- Default rate by risk band  
- Average profit per borrower by risk band  

These metrics were chosen because the goal of the project is decision-making, not just prediction accuracy.

## Key Findings
- The logistic regression model achieved a ROC-AUC of about 0.72 and provided a strong baseline.  
- The XGBoost model improved performance with a ROC-AUC of about 0.78.  
- Risk bands created from model predictions showed clear separation in default rates.  
- High Risk borrowers consistently produced large expected losses.  
- Low and Medium Risk borrowers remained profitable under the same approval policy.  

## Final Decision
Approval decisions are based on XGBoost-predicted default probabilities segmented into percentile-based risk bands. The model improves risk separation relative to logistic regression, leading to higher expected profitability under the same approval policy.

## Tools Used
- Python  
- pandas  
- scikit-learn  
- XGBoost  
- NumPy  
- Jupyter Notebook  
