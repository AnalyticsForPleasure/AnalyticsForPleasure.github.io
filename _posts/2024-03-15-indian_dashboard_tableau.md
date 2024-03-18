---
title: "Exploring the World of Indian Cuisine Through Analysis with Tableau"

categories:
- Tableau 
- Tableau & Python
tags:
- Indian Recipes Analysis
- Tableau
- Storytelling
- Viz
---

Today, I aim to blend two potent tools: **Python** (my usual go-to) and **Tableau** (as evidenced by my recent posts). Each excels in its own realm—**Python** *for analysis in the domains of data science and data analytics*, and **Tableau** *for visualization, catering to graphic artists/designers and data analysts alike*. By leveraging both, we'll explore how to extract maximum value from data analysis and craft unique dashboards. *Let's dive into the data aspect!*

For today's endeavor, I've chosen to delve into a dataset sourced from Kaggle titled **"Indian Food"**. *Comprising 9 columns and 255 rows*, it promises an interesting exploration.

Here are the columns names: 

![image-left]({{ 'assets/img/for_posts/indian_dashboard/column_names.png' | absolute_url }}){: .align-left}


Through this analysis, we'll uncover insights into the rich tapestry of Indian cuisine, unraveling its flavors and ingredients. So, let's embark on this journey of data discovery and visualization prowess, and unravel the story behind each culinary delight.



As usual, I will start with a sneak peek of the output dashboard about "Indian Food":


![image-left]({{ 'assets/img/for_posts/indian_dashboard/Full_indian_dashboard.png' | absolute_url }}){: .align-left}





For my initial analysis, I aim to focus on three key columns: **Name, Prep_time, and Cook_time**, which will be utilized to generate an output chart. Given the fundamental role of preparation and cooking times in crafting delicious dishes, the chart will display the duration of both stages for each dish. This analysis may reveal two distinct patterns: dishes characterized by lengthy preparation time but short cooking time, and conversely, dishes featuring brief preparation time but extended cooking time.


Let's now consider a subset of 13 dishes from the total of 255 dishes :

![image-left]({{ 'assets/img/for_posts/indian_dashboard/Cooking_time_preparation_time.png' | absolute_url }}){: .align-left}
