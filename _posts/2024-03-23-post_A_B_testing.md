---
title: "Analyzing Data with Python: A/B Testing"

categories:
- A/B Testing 
- Bucket Testing
- Split Testing
tags:
- Retention
- Cookie cats
- Retention Rate
- Bootstrapping
---

**Introduction - What is A/B testing?**

**A/B testing**, also known as split testing, is a method used to compare two versions of something to determine which one performs better. It's commonly used in various fields, including marketing, product development, and user experience optimization. In A/B testing, two versions (A and B) of a product, feature, or experience are shown to different groups of users, and their responses or behaviors are compared to identify which version is more effective in achieving the desired outcome.

![image-left]({{ '/assets/img/for_posts/AB_testing/Control_group_image.png' | absolute_url }}){: .align-left}

**How to use control group in A/B testing?**

*The control group in A/B testing serves as the baseline against which changes introduced in the experimental group are compared*. By maintaining existing conditions for this group, researchers can accurately *measure the impact of variations implemented in the experimental group*. Through random assignment and statistical analysis, the **control group helps ensure unbiased comparisons and valid interpretations of the experiment's results, guiding decision-making processes effectively.**


In a scenario where you're developing games for kids, conducting an A/B test *could involve comparing the performance or engagement of different versions or features of the game*. For example, you might want to test two versions of a puzzle game targeted at preschoolers, where one version introduces a new set of characters or challenges compared to the other. By randomly assigning children to either Version A or Version B of the game, you can measure metrics such as **completion time**, **number of levels completed**, or **player satisfaction** to determine which version yields better results. Through rigorous data analysis and statistical testing, **A/B testing provides valuable insights into which game version resonates more effectively with the target audience**, enabling game developers to make informed decisions about future iterations or updates. This iterative approach to game development helps optimize user experience and increase engagement, ultimately leading to a more successful product in the competitive market of kids' games.


Today, we'll delve into the data analysis of **'Cookie Cats**', a highly popular mobile puzzle game developed by Tactile Entertainment. This game follows the classic "connect three" puzzle format, where players connect tiles of the same color to clear the board and advance levels. As players progress, they may encounter gates that require either waiting a significant amount of time or making in-app purchases to proceed further. These gates not only serve to encourage in-app purchases but also offer players necessary breaks from gameplay, potentially enhancing their overall enjoyment and engagement with the game. However, determining the optimal placement for these gates is crucial. Let's begin by loading the data and examining the details.

Let's begin delving into the data:

![image-left]({{ '/assets/img/for_posts/AB_testing/Explanation_about_the_column_name.png' | absolute_url }}){: .align-left}




To kick off our data analysis, let's examine the first column, **"Userid"**. Our initial inquiry is whether each "Userid" is unique. 

Therefore, we will running the code bellow in order to find if there are not non - unique values:
```python
df["userid"].nunique()
```

**We find that there are 90,189 unique user IDs in our dataset ( The entire dataset)**


Moving on to the next column, **"sum_gamerounds"**.
we aim to understand the gaming activity of each user. Specifically, we 
want to determine:

>* The number of users who never played the game.

And

>* Identify any outliers that may skew our analysis.

Therefore, our first step is to determine the *number of users who never played*. We can accomplish this by executing the following code:

```python
Players_who_did_not_played = df[df["sum_gamerounds"]== 0]["userid"].count()
```

**We identify the count of players who did not engage in any game round.**


Now, let's proceed to identify and address any outliers within the dataset.
We analyze the distribution of game rounds played by users using 

```python
Number_of_game_rounds_played_by_each_player = df['sum_gamerounds'].value_counts().sort_values(ascending=False)
```

While most users have played up to around 3,000 game rounds, **we identify a rare observation where one user played an astonishing 49,854 rounds**. To maintain data integrity, *we opt to remove this outlier from the dataset to ensure accurate analysis and experimentation*.

Now, let's move on to the to the **"version"** column. This column present to us the 2 verions we want to check and make the A/B testing. Therefore, we would like to start with a short of info - A/B Groups & Target Summary Stats
 
Now, let's shift our focus to the 'version' column. This column represents the two versions we aim to compare in our A/B testing. To kick off, let's provide a brief overview of the A/B groups and summarize their target statistics.

Here's the output we got:

![image-left]({{ '/assets/img/for_posts/AB_testing/comparison_between_groups.png' | absolute_url }}){: .align-left}

**Reviewing the Summary Stats for the A/B groups:**

>* The group with the gate at **level 30 comprises 44,700 records**, while the group with the gate at **level 40 consists of 45,489 records**.

>* Notably, the group with the gate at level 30 exhibits a clear outlier, with one user having played **49,854 rounds** within 14 days of installing the game, while the next highest record is **below 3,000 rounds**.

>* Interestingly, the standard deviation of the Control group is higher than that of the Test group, with values of **256.7 and 103.3**, respectively.


The **'sum_gamerounds'** column holds crucial significance. Let's analyze the data in this column using a matplotlib chart:

<script src="https://gist.github.com/AnalyticsForPleasure/c5dde8944679568c808114c13dbb2751.js"></script>


In the following chart, **I aim to analyze players' progression through game rounds**. Specifically, I'm interested in understanding the distribution of player IDs across various milestones, such as the first, twentieth, and one hundred fiftieth rounds. Due to the low number of players in certain rounds, I've opted to use a **logarithmic scale on the Y-axis for clarity**. This scale allows for a more effective visualization of player distribution across rounds, as demonstrated below.

![image-left]({{ '/assets/img/for_posts/AB_testing/games_rounds_chart.png' | absolute_url }}){: .align-left}


Now, let's delve deeper into the analysis and shift our focus to the last two columns: '**retention_1**' and '**retention_7**'. In these columns, each row contains a boolean value - either 'True' or 'False'. So, what does this signify? Well, **retention measures the customers who continue to use a product or service over a specified period of time**.

Each row provides us with information on whether the player decided to return and continue playing or if they chose to quit playing. Consequently, a **high retention percentage indicates that a business is effectively retaining its customers, keeping them engaged and satisfied**. This is crucial for maintaining consistent revenue and fostering customer loyalty.

Hence, for each version (Gate 30 / Gate 40), we aim to determine the retention rate.

Here's an output chart comparing the retention rates between the two time periods:


![image-left]({{ '/assets/img/for_posts/AB_testing/games_rounds_chart_2.png' | absolute_url }}){: .align-left}