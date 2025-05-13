---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# layout: home

---
# Group 4 - Project Assignment B for DTU Course 02247
If you are interested in a more technical point of view regarding this topic, you can click on the link below the section "Explainer notebook link below". Our website with visualizations starts below the section "Website".

This project is presented by Søren (s216161), Johannes (204399) and Oliver (s214929).

# Explainer notebook link below

[Explainer notebook](notebooks/explainer.html)

# Website
<img src="Pictures/yelp-red-1920.jpg" alt="Yelp background" style="width: 100%; max-height: 400px; object-fit: cover;">

Yelp is a service, that makes the user able to publish reviews about all kinds of businesses. An article from Yelp for Business [^1] shows that 96% of people on Yelp compare different places before deciding where to go. A dataset from Yelp's website contains data about around 150.000 different business with around 7.000.000 reviews.    

In this project, we dive into Yelp data from Philadelphia to find patterns in how people leave restaurant reviews to explore when and where they say it. We explore questions like:

- What time of day are most reviews written?
- Do star ratings change depending on the time?
- Are there areas of the city with better restaurant experiences?
- Which business categories are the most popular, i.e. what type of food should you look for?

We use different kinds of visualizations, both simple charts and interactive tools, to help you explore the data yourself. In the end, this story will help you navigate the food scene in Philadelphia using real Yelp reviews from 2005 to 2022.

## The people of Phildelphia love their food
Philadelphia is a city known for its rich history and diverse culture, and its food scene is no exception. From cheesesteaks to soft pretzels, the city has a wide variety of culinary delights. But what do the people of Philadelphia really think about their food? To find out, we analyzed Yelp reviews from the city to see how people rate their dining experiences. 
When taking a look at the star ratings of the reviews left by users, we can see that the majority of reviews are rated 4 stars or higher. This suggests that people in Philadelphia generally have a positive view of their dining experiences. However, there are still a significant number of reviews rated 1 star, indicating that not all experiences are positive.
<figure>
  <img src="Pictures/star_rating_distribution.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 1:</strong> Distribution of star ratings in reviews of Philadelphia restaurants.</figcaption>
</figure>
However, when taking a look at the star ratings of the restaurants, we can see that the majority of restaurants are rated 3.5 stars or higher indicating that most restaurants in Philadelphia are rated positively. There are still a significant number of restaurants rated 3 stars or lower. In this project we will try and discover patterns that could explain which restaurants are rated positively and which ones are rated negatively.
<figure>
  <img src="Pictures/star_rating_distribution_businesses.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 2:</strong> Distribution of star ratings of Philadelphia restaurants.</figcaption>
</figure>

## When does people make their reviews?
A blog post from MadMobile[^2] says that the busiest time for restaurants is between 6 PM and 9 PM. You might think, that people using Yelp often write reviews after dinner or later at night when they get back home. The charts below shows that this is true in Philadelphia. Most reviews are written in the evening or late at night.

The first chart shows the overall count of all star rating based on Yelp reviews. 
<figure>
  <img src="Pictures/reviews_per_hour.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 3:</strong> Distribution of star rating per Hour of the day.</figcaption>
</figure>

This chart shows what time of day people leave reviews, split by star rating. The numbers are adjusted so we can compare them more fairly. That is important because, as we saw in Figure 1, there are a lot more high-star reviews than low-star ones. This chart helps us see the typical pattern for each rating.

<figure>
  <img src="Pictures/minmax_normalized_hourly_distribution.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 4:</strong> Five subplots showing the hourly distribution by each star rating.</figcaption>
</figure>

However, just like in Figure 3, we can see that most reviews, no matter the rating, are written in the evening or late at night.

Finally, we show an interactive chart below. Here you can toggle the different time blocks, and see which hours has which star rating and how it changes through the day. 

<figure>
  <iframe src="Pictures/review_counts_per_star_rating.html" width="1000" height="550"> </iframe>
  <figcaption><strong>Figure 5:</strong> Review counts per review across 3-hour blocks.</figcaption>
</figure>

The overall pattern looks very similar across all time blocks:

1. 1-star reviews are more common than 2-star reviews
2. 5 stars is the most frequently given rating in all time slots
3. 4-star reviews are more common than 3 stars, but less common than 5 stars
4. 3-star reviews appear more often than both 1- and 2-star reviews

# When should you go visit a restaurant in Philadelphia?

To address this question, we have tried to interpret three different restaurants. They are chosen based on being the three restaurants with the most variance in terms of different star ratings and by having at least 50 reviews. Businesses with a wide range of different reviews are especially interesting to investigate, as they might show stronger time-based trends. As an example, this can be used for Yelp users to determine at what time they should go to the restaurant. Please see the plots below and think about the results. 

<figure>
  <img src="Pictures/top_variable_businesses.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 6:</strong> Distribution of reviews per hour of the day for three restaurants.</figcaption>
</figure>
It is important to remember that these three restaurants have different opening hours. To find the best time to visit, we need to be careful as people might leave reviews long after they have eaten, so the review time does not always match the visit time. 

This chart shows how review scores change during the day for three restaurants. The ratings go up and down depending on the time. Pat’s Pizzeria gets better reviews at lunch and late evening. Love Park Pizza has lower scores in the early morning. Mangiamo 444 mostly gets reviews during opening hours, but some low scores come later, maybe when people write reviews after thinking about their visit.

Some weak conclusions based on these plots includes:
1. Based on the plot, a user might prefer to visit Pat’s Pizzeria either at lunchtime or late in the evening, as those are the times when reviews tend to be more positive.
2. Based on the trend, the best time to visit seems to be at the end of peak periods, like after lunch, dinner, or late-night hours. In contrast, this business appears to be a poor choice for breakfast, as early reviews tend to be lower.
3. Interestingly, the lowest ratings are typically posted outside of business hours. This could suggest that customers had time to reflect on their experience before writing a more critical review. However, there are also a few 5-star reviews posted in the morning, indicating that not all delayed reviews are negative.


## What food categories do the people of Philadelphia enjoy the most?
There are lots of different restaurants in Philadelphia each covering a wide range of food categories. But which ones are the most popular? To find out, we looked at the number of restaurants in each category. The top 24 categories are shown below.
<figure>
  <img src="Pictures/category_counts.png" alt="Star Rating Distribution" style="width:150%; max-width:1000px;">
  <figcaption><strong>Figure 8:</strong> The number of restaurants for each top 24 category.</figcaption>
</figure>
When ignoring 'Nightlife' and 'Bars' as these aren't known for their food options, it appears (based solely on the number of restaurants) that pizza and sandwiches are among the most popular categories in Philliadelphia. 

However, when taking a look at the distribution of the star ratings of the restaurants in each category it can be seen that sandwich restaurants are quite a bit more popular than the pizza ones. Pizza restaurants are however still having a generally positive star of rating of the majority of the restaurants having averages above 3.0. This is not the case for burger restaurants that appear to be the worst performing. Here it can be seen that there is quite a siginificant amount of 2 star rated businesses. On the other hand japanese food is extremely popular with having one of the most right leaning curves. 


All in all it can be hard to conclude anything with certainty based on the distribution alone. Firstly. the number of restaurants vary a lot and can give unfair comparisons. Secondly, some categories, such as burgers, are more represented in the fastfood industry which isn't known for it's quality of food. This can make comparisons to categories, such as japanese, a bit unfair as these usually have a reputation for being of higher quality. 

<figure>
  <iframe src="Pictures/restaurant_star_ratings_distribution.html" width="1000" height="750"> </iframe>
  <figcaption><strong>Figure 7:</strong> Distribution of star ratings for different restaurant categories.</figcaption>
</figure>

# Where should you go?

<figure>
  <iframe src="Pictures/philadelphia_restaurant_map.html" width="1300" height="750"> </iframe>
  <figcaption><strong>Figure 9:</strong> Areas of Philadelphia and their average rating along with individual restaurants.</figcaption>
</figure>

# Discussion
In this project, we looked at Yelp reviews in Philadelphia to help you guys to decide where to eat, what kind of food to try, and when to go. We have used different types of charts so you can explore the data yourself.

By focusing on just one city, the results were easier to understand. Looking at ratings by category, time, and location gave us a good overview of the restaurant situation.

There are still things that could be better. Review times do not always show when people actually ate at the restaurant, so time-based patterns might not be 100% accurate. We also did not look at the review text or information about the users, which could have given more insight.

Overall, the project tells a clear and helpful story using data, which gives people a fun way to explore food in Philadelphia.

# References
[^1]: https://business.yelp.com/resources/articles/study-shows-high-intent-consumers-are-contacting-businesses-quickly-on-yelp/?domain=local-business
[^2]: https://madmobile.com/blog/the-golden-hour/#:~:text=From%206%20to%209%20p.m.,to%20make%20the%20most%20revenue.