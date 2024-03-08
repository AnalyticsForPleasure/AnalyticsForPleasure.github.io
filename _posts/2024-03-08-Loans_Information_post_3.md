---
title: "Loan Insights Unlocked ( Post 3 of 3 )"

categories:
- Loans 
tags:
- Credit Risk
- Financial Information
- Interest Rate
---

Today we will continue with analyzing the Kaggle dataset titled **‘Comprehensive Loan Information for Credit Risk’**.  

As we go over the dataset we can notice 2 super important columns: **“sub_grade”** and **“grade”**. Those columns are related to the loans grading system. 

The loans grading system is a method used by lenders and investors to evaluate the creditworthiness and risk level of individual loans. It categorizes loans into different grades and sub-grades based on *various factors such as the borrower's credit history, income, debt levels, and other risk indicators*.


**Grades (A through G):**
* Loans are typically categorized into seven main grades, labeled from A through G.
* Each grade represents a different level of credit risk, with Grade A loans being the least risky and Grade G loans being the most risky.


**Sub-Grades (1 through 5):**
* Within each main grade, there are usually sub-grades numbered from 1 to 5.
* Sub-grades further refine the risk assessment within each grade, providing a more nuanced evaluation of credit risk.


Now, Let’s explain about the Critical Role and Importance of the grading system:

**Risk Evaluation:**
The grading system's central objective is to evaluate the credit risk inherent in each loan. Both lenders and investors rely on these grades to assess the likelihood of borrowers meeting their repayment obligations promptly and completely.

**Interest Rate Determination:**
Loans assigned higher grades usually incur lower interest rates, mirroring the perceived lower risk level associated with them. Conversely, loans with lower grades may carry higher interest rates to offset the heightened risk exposure.
Investment Strategy Formulation:

Investors leverage loan grades to formulate well-informed investment strategies. This involves strategically allocating capital across different grades to construct a diversified portfolio that aligns with their risk tolerance and desired return objectives.

**Loan Pricing Strategy:**
Lenders utilize the grading system to devise pricing strategies for their various loan offerings. Higher-graded loans may enjoy more favorable terms and conditions, while lower-grade loans may be subject to higher fees or stricter eligibility criteria.


After providing a detailed overview, let's now delve into the code to analyze the number of loans at each level. Below is the code I've prepared for this purpose:


<script src="https://gist.github.com/AnalyticsForPleasure/efa955c75d1b2a9e6eb5fe47887b272b.js"></script>

Let's see now the output result : 




![image-left]({{ 'assets/img/for_posts/Comprehensive_Loan_Information/post_3/grid_matrix_style.png' | absolute_url }}){: .align-left}



![image-left]({{ 'assets/img/for_posts/Comprehensive_Loan_Information/post_3/grade_loans.jpg' | absolute_url }}){: .align-left}






<script src="https://gist.github.com/AnalyticsForPleasure/de041608cb55d707bfdef108406f6232.js"></script>


![image-left]({{ 'assets/img/for_posts/Comprehensive_Loan_Information/post_3/Loan_purpose_and_Intrest_rates.png' | absolute_url }}){: .align-left}


