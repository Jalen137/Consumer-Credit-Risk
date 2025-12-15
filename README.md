# Consumer-Credit-Risk
Estimating the chance that someone will not pay back their loan. Then I will take this information and decide whether to give them the loan or not. 

## Business Question
How do we decide which applicants to approve for credit while mitigating the default losses and maximizing our companies profit? 


## Project Overview
This project's purpose is to build a credit risk model to estimate the probability of default for loan applicants and uses that risk to make approval decisions that balance the profit in the loss from the loans. 


## Mock company 
This analysis is framed around a mock medium-sized consumer lending company that gives out personal loans. The company wants to grow revenue while controlling default losses. 

## Dataset

Where it comes from
Got it from the UC Irvine Machine Learning Repository
https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients

What it represents

Why I chose it

### Dataset Discription
This research employed a binary variable, default payment (Yes = 1, No = 0), as the response variable. This study reviewed the literature and used the following 23 variables as explanatory variables:
X1: Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit.
X2: Gender (1 = male; 2 = female).
X3: Education (1 = graduate school; 2 = university; 3 = high school; 4 = others).
X4: Marital status (1 = married; 2 = single; 3 = others).
X5: Age (year).
X6 - X11: History of past payment. We tracked the past monthly payment records (from April to September, 2005) as follows: X6 = the repayment status in September, 2005; X7 = the repayment status in August, 2005; . . .;X11 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; . . .; 8 = payment delay for eight months; 9 = payment delay for nine months and above.
X12-X17: Amount of bill statement (NT dollar). X12 = amount of bill statement in September, 2005; X13 = amount of bill statement in August, 2005; . . .; X17 = amount of bill statement in April, 2005. 
X18-X23: Amount of previous payment (NT dollar). X18 = amount paid in September, 2005; X19 = amount paid in August, 2005; . . .;X23 = amount paid in April, 2005.

## How I went about the project
- Look for a good dataset
- Data cleaning fitting
- Default prediction model
- Risk-based approval rules


## Decision Framework


## Evaluation Metrics


## Key Findings


## Tools Used
