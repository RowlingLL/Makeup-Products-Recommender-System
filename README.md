# Makeup-Products-Recommender-System
Goals¶
To build several recommender systems for current users and potential users with different approaches:

Demographic filtering: based purely on overall ratings of products

Collaborative filtering: based on user-item interaction history

Content based filtering: based on product features and user features -- in progress

Hybrid model: based on user feature, item feature, and interaction, potentially recommending products to new users according to user input -- in progress

Dataset overview
This system used a private dataset scrapped from https://www.sephora.com containing product details and user reviews history, including 13K products, 210K users, 325K reviews. I've put them into 2 csv files:

'all_primary_products.csv':

product_id: product identifier
sku_id: identifier for different colors within one product
category: category this product belongs to, i.e. eye, face, lip...
name: prodcut name
brand: product brand
price: product price at the time of webcrawling
product_url: product url
image_url: url of the main product image
rating: overall average rating
reviews_count: number of reviews on this product
loves_count: number of 'love' clicked on this product
color_count: color counts of the product, if any. e.g. accessories normally have 0 colors, but foundations could have several different colours
details: detailed product discription
sku_group: different colors within one product
similar_products: similar products defined by merchant
bought_together: products that usually bought together
is_listed: whether the product is available at the time of webcrawling

'all_users_reviews.csv':

product_id: product identifier
product_name: prodcut name
product_url: product url
user_nickname: user nickname
author_id: user identifier 
location: user location
eye_color: user eye color on file 
hair_color: user hair color on file
skin_tone: user skin tone on file
skin_type: user skin type on file
age_range: user age range on file
rating: rating this user gave to this product, on scale 1-5
review_title: title of user review
review_text: text of this review
is_recommended: whether this user recommend this product, '1' recommend, '0' not recommend
submission_time: time of the review submission
helpful_count: number of people who think this review is helpful
not_helpful_count: number of people who think this review is not helpful
helpfulness: helpful_count/(helpful_count+not_helpful_count)
