# Food Trends

## Introduction
The concept of 'going viral' was first introduced in the 1970s to explain how ideas and information spread from person to person within social networks. Since then, and in large part due to the advent of the internet and social media, the concept of 'going viral' has become ubiquoutous in our society. Some strive to go viral and gain notoreity, while others hope to remain below the radar. 

Yet the impact of viral posts cannot be understated. Sometimes virality can be dangerous- remember the TidePod challenge- but frequently it can be used by individuals and businesses to build a following and customer base. 

One area that sees trends driven by viral food posts is the food industry. Restaurants have seen their success driven by one viral food item and groceries stores have seen shortages of ingredients that are featured in viral recipes. In short, food trends effect all of us. 

Based on the text of the post title, can we predict if a food post will go viral? Understanding if a food post will go viral can be beneficial to restaurants so that they can prepare inventory and staffing and grocery stores so that they can stock ingredient appropriately. Companies that manufacture food items or ingredients will also benefit from this predicitve capability to up supply if needed and join in their marketing efforts.

## Methods
Data was sourced from the Reddit subreddit forum r/food using the pushshift API and the Reddit API.

Various models were explored to identify the highest performing model through trial and error. Models with relatively high performance were tuned using grid search to identify the best hyperparameters.

## Data Dictionary
The final data set used in the modeling is stored in the 'posts_scores_dates.csv' files stored in the data folder.

|Feature|Type|Description|
|---|---|---|
|id|object|Post Submission ID- unique identifier|
|title|object|Text content of the post title|
|created_utc|int|Original timestamp of post-submission|
|post_time_est|datetime|Converted timestamp of post-submission from UTC to EST|
|score|float|Total number of 'upvotes' a post received, used as a proxy for 'viralness'|
|comments|float|Total number of comments a post received, used as a proxy for engagement|
|percentile|float|Ranking of the post's score relative to all posts|
|viral|int|Binary indicator of if a post is 'viral' (1) or not (0). Viral is defined at the top 2% of all posts|

## Limitations
While the reddit posts include photogrpahs this analysis is limited to the text included in the post title. It is possible that users are incentivized to upvote a post more by the photo than the text. Further research can be conducted on the image data and the text data combined.

Additionally, this analysis is limited to Reddit posts. When an idea or food goes truly viral it spreads across social media and beyond social media to traditional media and interpersonal connections. This analysis cannot be applied to other social media platforms or other forms of communication. Fruther research can be conducted to map the spread of trends between social media platforms and beyond.

## Further Research
Sources
- https://towardsdatascience.com/an-extensive-guide-to-collecting-tweets-from-twitter-api-v2-for-academic-research-using-python-3-518fcb71df2a

- https://www.eater.com/a/viral-food-instagram-rainbow-bagels-cronuts?_gl=1*pw8eqn*#theory_title_page

- https://github.com/praw-dev/praw

- https://www.fox5ny.com/news/viral-tiktok-video-recipe-prompts-feta-cheese-shortage