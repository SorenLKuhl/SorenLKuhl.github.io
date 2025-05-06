---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# layout: home

---
# Get inspired
[YOLO](https://www.youtube.com/watch?v=KWMyxIHmReE&pp=ygULbmVkZSBzw7hyZW4%3D)

# Explainer notebook link below

[Explainer notebook](notebooks/explainer.html)

# Website
<img src="Pictures/yelp-red-1920.jpg" alt="Yelp background" style="width: 100%; max-height: 400px; object-fit: cover;">

In this project, we dive into Yelp data from Philadelphia to find patterns in how people leave restaurant reviews, not just what they say, but when and where they say it. We explore questions like:

- What time of day are most reviews written?
- Do star ratings change depending on the time?
- Are there areas of the city with better restaurant experiences?
- Which business categories are the most popular?

We use different kinds of visualizations, both simple charts and interactive tools, to help you explore the data yourself. In the end, this story will help you navigate the food scene in Philadelphia using real Yelp reviews from 2005 to 2022.

## The people of Phildelphia love their food
Philadelphia is a city known for its rich history and diverse culture, and its food scene is no exception. From cheesesteaks to soft pretzels, the city has a wide variety of culinary delights. But what do the people of Philadelphia really think about their food? To find out, we analyzed Yelp reviews from the city to see how people rate their dining experiences. 
When taking a look at the star ratings of the reviews left by users, we can see that the majority of reviews are rated 4 stars or higher. This suggests that people in Philadelphia generally have a positive view of their dining experiences. However, there are still a significant number of reviews rated 1 star, indicating that not all experiences are positive.
<figure>
  <img src="Pictures/star_rating_distribution.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 1:</strong> Distribution of star ratings in Philadelphia restaurants.</figcaption>
</figure>

<figure>
  <img src="Pictures/star_rating_distribution_businesses.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 2:</strong> Distribution of star ratings in Philadelphia restaurants.</figcaption>
</figure>


## What food categories do the people of Philadelphia enjoy the most?
There are lots of different restaurants in Philadelphia each covering a wide range of food categories. But which ones are the most popular? To find out, we looked at the number of restaurants in each category. The top 24 categories are shown below.



## When does people make their reviews?
A blog post from MadMobile[^1] says that the busiest time for restaurants is between 6 PM and 9 PM. You might think, that people using Yelp often write reviews after dinner or later at night when they get back home. The charts below shows that this is true in Philadelphia. Most reviews are written in the evening or late at night.

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

<figure>
  <iframe src="Pictures/restaurant_star_ratings_distribution.html" width="1000" height="750"> </iframe>
  <figcaption><strong>Figure 7:</strong> Distribution of star ratings for different restaurant categories.</figcaption>
</figure>

<figure>
  <img src="Pictures/category_counts.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 8:</strong> The number of restaurants for each top 24 category.</figcaption>
</figure>

# References 
[^1]: https://madmobile.com/blog/the-golden-hour/#:~:text=From%206%20to%209%20p.m.,to%20make%20the%20most%20revenue.