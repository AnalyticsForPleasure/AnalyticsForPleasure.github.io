---
title: "Unlocking Insights: A Comprehensive Guide to Loan Analysis"


categories:
- Loans 
tags:
- Credit Risk
- Financial Information
- Interest Rate
---

Today, we're delving into a financial dataset centered on the topic of *'Loans'*. Obtained from Kaggle, this dataset titled **['Comprehensive Loan Information for Credit Risk']**(https://www.kaggle.com/datasets/nezukokamaado/auto-loan-dataset) comprises an extensive array of *data with 24 columns and 38,576 rows*.

Here's a quick overview of the column names:
* 'id', 'address_state', 'application_type', 'emp_length', 'emp_title', 'grade', 'home_ownership', 'issue_date', 'last_credit_pull_date', 'last_payment_date', 'loan_status', 'next_payment_date', 'member_id', 'purpose', 'sub_grade', 'term', 'verification_status', 'annual_income', 'dti', 'installment', 'int_rate', 'loan_amount', 'total_acc', 'total_payment'

Before diving into the dataset's analysis, let's start with a fundamental question: **"What exactly is a loan?"**


> A loan is a financial arrangement in which one party, typically a lender such as a bank or financial institution, provides money or assets to another party, known as the borrower. The borrower agrees to repay the loan amount over time, usually with added interest or fees. 
Loans can be used for various purposes, such as purchasing a home, financing education, starting a business, or covering personal expenses. 
The terms of the loan, including the **amount borrowed, interest rate, repayment schedule, and any collateral required**, are typically outlined in a legal contract between the lender and the borrower.




Now that we've clarified the concept, let's delve into analyzing the dataset. We're poised to explore some intriguing questions today.

We'll kick off with our first inquiry. As we're all aware, the United States comprises 50 states. As we peruse the dataset, I'm curious: **In which state do residents take out the most loans?**

Some may initially suggest states with higher poverty rates, such as Mississippi, Louisiana, and West Virginia, assuming they have the highest loan rates. However, let's reserve judgment and allow the analysis to speak for itself as we examine the data.

Upon initial review, it appears that those *who anticipated a correlation between high poverty rates and increased loan uptake were mistaken*. Surprisingly, the **top states for loan acquisition are California, New York, Florida, Texas, and New Jersey**, which diverges from our initial assumptions.

![image-left]({{ 'assets/img/for_posts/Comprehensive_Loan_Information/post_1/treemap_count_for_each_state.jpg' | absolute_url }}){: .align-left}

There could be numerous factors at play here. Firstly, it's evident that the prevalence of loans isn't directly tied to poverty rates as previously presumed. Supporting evidence can be found in a comparison with data from sources like Wikipedia's **"List of U.S. states and territories by poverty rate"**.

For instance, *New York ranks 19th* with a poverty rate of **13.58%**, *Texas sits at 14th* with **14.22%**, *California holds 26th place* with a poverty rate of **12.58%**, *Florida ranks 20th* with a poverty rate of **13.34%**, and **New Jersey stands at 47th with a poverty rate of 9.67%**.