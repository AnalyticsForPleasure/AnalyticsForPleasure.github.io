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


Moving on to the next column, **"sum_gamerounds"**, we aim to understand the gaming activity of each user. Specifically, we want to determine:

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

While most users have played up to around 5,000 game rounds, **we identify a rare observation where one user played an astonishing 49,854 rounds**. To maintain data integrity, *we opt to remove this outlier from the dataset to ensure accurate analysis and experimentation*.