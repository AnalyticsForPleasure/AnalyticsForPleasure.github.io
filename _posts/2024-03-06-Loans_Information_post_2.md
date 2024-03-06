---
title: "Loan Insights Unlocked ( Post 2 of 3 )"

categories:
- Loans 
tags:
- Credit Risk
- Financial Information
- Interest Rate
---


In our previous discussion, we explored two primary inquiries: identifying the states where residents tend to borrow the most and determining the most active loan-taking region among the Northeast, West, Southeast, Midwest, and Southwest.

As we delve further into the dataset, we encounter an intriguing variable: **"annual_income"**. This prompts me to pose the following question: 

**Could there be a relationship between the average income in different regions and the frequency of loans taken out?**


Consequently, I aim to examine the *relationship between the number of loans and average income for each region* (Midwest, Northeast, Southeast, Southwest, and West, as previously defined). Specifically, I seek to understand whether regions with higher average incomes exhibit a higher frequency of loan acquisitions. Conversely, do regions with lower average incomes experience fewer loan transactions?

Hence, as a follow-up to the second question posed in the previous post, I intend to address this inquiry by implementing the following code.

<script src="https://gist.github.com/AnalyticsForPleasure/409a21926cd3d46dd6b519f1d8ca9abf.js"></script>

Now, let's take a look at the resulting output:

![image-left]({{ 'assets/img/for_posts/Comprehensive_Loan_Information/post_2/style_table.png' | absolute_url }}){: .align-left}



![image-left]({{ 'assets/img/for_posts/Comprehensive_Loan_Information/post_2/image_Question_4.jpg' | absolute_url }}){: .align-left}




Let's delve into another intriguing aspect of our analysis: **exploring the influence of employment duration, as captured by the 'emp_length' column, on the borrowing behavior of individuals**. This prompts a thought-provoking line of inquiry: **How does the length of employment impact the decisions surrounding loan acquisition?**

Consider the scenario where an individual has been employed for only 2 years compared to another who boasts 9 years of service in the same role. *Is there a discernible difference in their likelihood to secure larger loans?* Furthermore, *what can we glean about the average loan amounts taken by individuals with varying lengths of employment, such as those with 6 years versus 3 years of employment?*

These questions not only pique our interest but also offer valuable insights into the dynamics between employment stability and financial decisions. By unraveling these intricacies, we gain a deeper understanding of the complex interplay between employment duration and borrowing behavior.

To embark on this exploration, let's dive into the code and dissect the relationship between employment duration and loan acquisition.




![image-left]({{ 'assets/img/for_posts/Comprehensive_Loan_Information/post_2/image_boxplot_Question_5.jpg' | absolute_url }}){: .align-left}
