# Sentiment-Analysis

Web Scraping and Sentiment Analysis With Python, Selenium, TextBlob and OpenAI

Step 1 — Web Scrape to Get Reviews
We need to perform web scraping to get User Reviews on IMDb. Beautiful Soup and Selenium can be used for this task. In case you ask, below is a brief introduction about these two:
- Beautiful Soup is a Python library that is primarily used for parsing and extracting data from HTML and XML documents. It provides a simple and intuitive interface to navigate and search the parse tree created from the document.
- Selenium is a powerful tool for automating web browsers. It provides a browser automation framework that allows you to control web browsers programmatically. Selenium enables tasks such as simulating user interactions, filling out forms, clicking buttons, and navigating through web pages.
- Prompt: Web scrape [https://www.imdb.com/title/tt27528139/reviews?ref_=tt_urv](https://www.imdb.com/title/tt1517268/reviews) to get all reviews with Python, BeautifulSoup, and Selenium. 25 reviews are displayed per page. In order to see more reviews, I need to click on the Load More button. Store the result in imdb_reviews.csv

Step 2 — Sentiment Analysis with TextBlob
- Skimming the reviews, I see that most are negative and with a rating of 1/10. As our goal is to find positive aspects of this series, we need to filter only the positive reviews. For this purpose, we can rely on user ratings or perform sentiment analysis. The second option is used in this post. Why? Sentiment analysis algorithms analyze the text to assess whether it conveys a positive, negative, or neutral sentiment. This approach allows for a more nuanced understanding of the sentiment expressed in a review. Sentiment analysis can capture subtle aspects of the text and provide insights beyond just an overall rating. It can help identify positive reviews that might have lower ratings due to specific reasons or negative reviews that mention positive aspects.
- TextBlob is a great Python library that we can use for this sentiment analysis. TextBlob uses a machine learning algorithm to classify text into positive and negative sentiments.
- Prompt: imdb_reviews.csv stores all movie reviews in the column Review. Use TextBlob to perform sentiment analysis for these reviews and give me the top 10% of positive reviews.

Step 3 — Summarize Positive Reviews with OpenAI
- In this final step, we need to capture key information and important details in these reviews. OpenAI is capable of doing this task.
- To keep it easy to follow, the code of Step 2 is included as well.
- Note: increase the max_token if you want to have a longer summary.
