## Project: Web APIs & Classification


### Project: Space x vs Blue Origin  

I pulled Reddit posts using keywords: spacex and blueorigin.
- 989 posts of space x
- 977 posts of blue orgin

#### Steps
- Utilized Reddit API to do web scrapping
- Converted Jason file into DataFrame
- Applied NLP on the posts, including removing punctuations, bag-of-words model, removing stop words and lemmatizing words
- Used Pipeline and GridSearch to apply CountVectorizer and Tf-IdfVectorizer on 4 different classification models and found best parameters for each model (8 models in total)
- Extracted Insights from models- mainly Logistic Regression and Naive Bayes
- Data Visualization
- Background search & Presentation

#### Limitations- to-do in the future
- I'll check accuracy of base line model to show that my model works good
- I'll try to remove two most powerful keywords and train the model again to see how it works differently
- I'll try to create my own stop words list 
- I'll pick up the FP/FN posts and analyze why they were misclassified

---

#### About the API

Reddit's API is fairly straightforward. For example, if I want the posts from [`/r/boardgames`](https://www.reddit.com/r/boardgames), all I have to do is add `.json` to the end of the url: https://www.reddit.com/r/boardgames.json

Reddit will give you 25 posts **per request**. To get enough data, you'll need to hit Reddit's API **repeatedly** (most likely in a `for` loop). _Be sure to use the `time.sleep()` function at the end of your loop to allow for a break in between requests. However, the API will cap you at 1,000 posts for each subreddit (assuming the subreddit has that many posts).

**Pro tip:** At the end of each loop, be sure to save the results from your scrape as a `csv`: JSON from Reddit > Pandas DataFrame > CSV. That way, if something goes wrong in your loop, you won't lose all your data.

To help you get started, there is a primer video on how to use Reddit's API: https://www.youtube.com/watch?v=5Y3ZE26Ciuk
