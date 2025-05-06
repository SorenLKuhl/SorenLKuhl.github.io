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

We use different kinds of visualizations, both simple charts and interactive tools, to help you explore the data yourself. In the end, this story will help you navigate the food scene in Philadelphia using real Yelp reviews.

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


<figure>
  <img src="Pictures/reviews_per_hour.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 3:</strong> Distribution of star rating per Hour of the day.</figcaption>
</figure>

<figure>
  <img src="Pictures/minmax_normalized_hourly_distribution.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 4:</strong> Five subplots showing the hourly distribution by each star rating.</figcaption>
</figure>


<figure>
  <img src="Pictures/top_variable_businesses.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 5:</strong> Distribution of reviews per hour of the day for three restaurants.</figcaption>
</figure>

<figure>
  <iframe src="Pictures/review_counts_per_star_rating.html" width="1000" height="550"> </iframe>
  <figcaption><strong>Figure 6:</strong> Review counts per review across 3-hour blocks.</figcaption>
</figure>

<figure>
  <iframe src="Pictures/restaurant_star_ratings_distribution.html" width="1000" height="750"> </iframe>
  <figcaption><strong>Figure 7:</strong> Distribution of star ratings for different restaurant categories.</figcaption>
</figure>

<figure>
  <img src="Pictures/category_counts.png" alt="Star Rating Distribution" style="width:100%; max-width:600px;">
  <figcaption><strong>Figure 8:</strong> The number of restaurants for each top 24 category.</figcaption>
</figure>