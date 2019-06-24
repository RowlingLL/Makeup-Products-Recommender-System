# Makeup-Products-Recommender-System
### Goals¶
To build several recommender systems for current users and potential users with different approaches:

> __Demographic filtering:__ based purely on overall ratings of products

> __Collaborative filtering:__ based on user-item interaction history

> __Content based filtering:__ based on product features and user features -- in progress

> __Hybrid model:__ based on user feature, item feature, and interaction, potentially recommending products to new users according to user input -- in progress

### Dataset overview
This system used a private dataset scrapped from https://www.sephora.com containing product details and user reviews history, including 13K products, 210K users, 325K reviews. I've put them into 2 csv files:

__'all_primary_products.csv':__

__product_id:__ product identifier<br>
__sku_id:__ identifier for different colors within one product<br>
__category:__ category this product belongs to, i.e. eye, face, lip...<br>
__name:__ prodcut name<br>
__brand:__ product brand<br>
__price:__ product price at the time of webcrawling<br>
__product_url:__ product url<br>
__image_url:__ url of the main product image<br>
__rating:__ overall average rating<br>
__reviews_count:__ number of reviews on this product<br>
__loves_count:__ number of 'love' clicked on this product<br>
__color_count:__ color counts of the product, if any. e.g. accessories normally have 0 colors, but foundations could have several different colours<br>
__details:__ detailed product discription<br>
__sku_group:__ different colors within one product<br>
__similar_products:__ similar products defined by merchant<br>
__bought_together:__ products that usually bought together<br>
__is_listed:__ whether the product is available at the time of webcrawling<br>

__'all_users_reviews.csv':__

__product_id:__ product identifier<br>
__product_name:__ prodcut name<br>
__product_url:__ product url<br>
__user_nickname:__ user nickname<br>
__author_id:__ user identifier <br>
__location:__ user location<br>
__eye_color:__ user eye color on file <br>
__hair_color:__ user hair color on file<br>
__skin_tone:__ user skin tone on file<br>
__skin_type:__ user skin type on file<br>
__age_range:__ user age range on file<br>
__rating:__ rating this user gave to this product, on scale 1-5<br>
__review_title:__ title of user review<br>
__review_text:__ text of this review<br>
__is_recommended:__ whether this user recommend this product, '1' recommend, '0' not recommend<br>
__submission_time:__ time of the review submission<br>
__helpful_count:__ number of people who think this review is helpful<br>
__not_helpful_count:__ number of people who think this review is not helpful<br>
__helpfulness:__ helpful_count/(helpful_count+not_helpful_count)<br>
