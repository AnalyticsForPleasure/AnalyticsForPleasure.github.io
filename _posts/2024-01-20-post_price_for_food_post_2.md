---
title: "Analyzing the Price Trends of Dairy Products in Israel Across"

categories:
  - Economic stats 
tags:
  - Prices

---



Today, our analysis extends to Kaggle-derived data, providing insights into the pricing trends of food items in Israel spanning several decades.

In the initial post, the focus was on **vegetables, fruits, meat, fish, and chicken**, revealing noteworthy price jumps every five years. Now, I aim to explore a different category of products—specifically, the pricing dynamics of **dairy products** in Israel. Consequently, I've chosen six items to investigate, ordered based on their price differences over a 15-year period.

The selected dairy products under examination are: 


* *Hard yellow cheese from cow's milk (100 g)*
* *Leben (200 ml)*
* *Cottage cheese' (250 grams)*
* *Soft white cheese (250 grams)*
* *Margarine for spreading in a cup (250 grams)*
* *Natural yogurt in a plastic container (200 ml)*


To analyze this, I wrote a code to obtain the output result. Here is the code I implemented:

<script src="https://gist.github.com/AnalyticsForPleasure/9b5b96b93e76705a6979dcfed2c3ae2f.js"></script>



Therefore, in the chart displayed below, I have analyzed the performance of these dairy products, plotting the data on a scale from the year 2009 to 2022. The **chart on the left**, titled "The Annual Variance of Dairy Product Prices over a 15-Year Period," presents a 14*6 matrix. Each matrix cell provides information on the percentage increase in price between the current price of a specific dairy product and the price of the same dairy product in the previous year.

Additionally, for each contiguous year, a green rectangle has been added, indicating the highest percentage among the 6 products for that specific year.

The **chart on the right**, under the title "Which Product Experienced the Highest Price Growth Each Year?" offers a clearer depiction of the dairy product with the most significant price increase in a given year. For instance, it answers questions like, "Which dairy product had the highest price increase over the entire period?" The answer, as illustrated, is **"Margarine (250 grams)"**. Similarly, if one wonders which dairy product held the title for the most consecutive years, the answer is also **"Margarine (250 grams)"**, observed between the years 2014 and 2017.

![image-left]({{ 'assets/img/for_posts/food_prices/question_3/heatmap_with_cow_2.png' | absolute_url }}){: .align-left} 







In the chart below, our objective was to identify the dairy product that experienced the most significant price decrease each year. Consequently, I have marked it with a red rectangle for clarity.

![image-left]({{ 'assets/img/for_posts/food_prices/question_3/heatmap_with_cow_3.png' | absolute_url }}){: .align-left} 