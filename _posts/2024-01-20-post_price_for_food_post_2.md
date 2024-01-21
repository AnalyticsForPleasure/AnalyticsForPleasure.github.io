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




Thus, in the chart displayed below, I have scrutinized the performance of these dairy products, representing the data on a scale spanning from 2009 to 2022. The left chart, titled "The annual variance of Dairy Product Prices over a 15-year period," comprises a 14*6 matrix. Each cell within this matrix provides information on the percentage increase in price from the current year to the preceding year for a specific dairy product.

Additionally, for each contiguous year, I have included a green rectangle, pinpointing the dairy product with the highest percentage increase among the six products for that particular year.

On the left side chart, titled "Which product experienced the highest price growth each year?," a clearer depiction emerges regarding the dairy product with the most significant price change each year. For instance, it reveals which dairy product experienced the highest price increase over the entire period—highlighted by "Margarine (250 grams)." It also indicates which dairy product earned the title for the most consecutive years, with the answer being "Margarine (250 grams)" between 2014 and 2017.

![image-left]({{ 'assets/img/for_posts/food_prices/question_3/heatmap_with_cow_2.png' | absolute_url }}){: .align-left} 







In the chart below, our objective was to identify the dairy product that experienced the most significant price decrease each year. Consequently, I have marked it with a red rectangle for clarity.

![image-left]({{ 'assets/img/for_posts/food_prices/question_3/heatmap_with_cow_3.png' | absolute_url }}){: .align-left} 