# SentimentAnalysis-FAANG

## AIM:
    The objective of this project is to perform Sentiment Analysis on the recent financial news headlines, 100 each of the 
    FAANG(Facebook, Amazon, Apple, Netflix, Google) stocks, to depict the emotion behind the headline and hence get to know 
    whether the market is feeling good or bad about a stock. Additionally, a word cloud is also generated to show the most 
    used words in the 100 headlines of a stock.

## PROCESS:
#### 1. Data Collection and Scraping:
- Sourced from the site FinViz.com. The site has been chosen since it contains headlines from trusted sources and not independent bloggers in addition to the headlines being similar in length and format.
- The data is scraped from the aforementioned site using BeautifulSoup and the requests module.
#### 2. Data Cleaning:
- From the site, we scrape the entire headline(inclusive of date) for every ticker.
- The most recent 100 headlines for every ticker and are stored in a dictionary.
- We then create a single pandas dataframe which stores the ticker, date, time and headline of all
the stocks. All similar headlines for a ticker are removed from the dataframe.
#### 3. Sentiment Analysis:
- The polarity of each headline is calculated using the ‘vader’ algorithm imported from the ‘nltk’ package. Each headline is analysed for its polarity score on a scale of -1 to 1, with -1 being highly negative and highly 1 being positive. This score is calculated by adding up the intensities of the words.
- The SentimentIntensityAnalyser function computes the positive, negative, neutral and scores of a word(string) passed to it. It also computes a compound score obtained through normalizing the previous three scores.
#### 4. Word Cloud Generation:
- Use the stored headlines of a stock and join them to form one single string.
- Remove all ‘,’ and ‘.’ from the text and create a general format by only capitalising the first
letter of every word with the remaining letters being lowercase.
- Make use of the package wordcloud and matplotlib to complete this process.
- Also show a bar graph depicting top 10 most commonly used words for that stock.

## CONCLUSION:
    With the main focus on analysing the emotions behind a headline, the following results have been shown in this project:
    • The mean sentiment of every stock based on the recent 100 headlines is generated.
    • The sentiment of a stock for a day is depicted on a graph based on the number of headlines on that date.
    • A word cloud of the most used words of the recent 100 headlines for a stock is generated.
    • The top 10 words in the recent 100 headlines for a stock is depicted in a bar graph.
