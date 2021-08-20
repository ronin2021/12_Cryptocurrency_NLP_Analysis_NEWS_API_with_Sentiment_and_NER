# 12_Cryptocurrency_NLP_Analysis_NEWS_API_with_Sentiment_and_NER
Analysis of Bitcoin and Ethereum articles written via NEWS api and using Sentiment and Named Entity Recognition(NER)


This is an application of Natural Language Processing (NLP) on content of the news aticles extracted from NEWS Api for Bitcoin and Ethereum.     

#### Part 1. Sentiment Analysis
1. Text contents of all current articles were obtained from NEWS Api for "Bticoin" and "Ethereum".
2. These text were then stored on to seperate dataframes.
3. Each of the text contents wre anayzed for sentiment via NTLK Vader to obtain statistical discriptions for compound, positive, negative, and neutral.

Following is a summary of the findings:

Q: Which coin had the highest mean positive score?

A: Bitcoin has mean positive score of 0.0547 while Ethereum has a mean positive score of 0.0433. Therefore the highest mean positive is with Bitcoin.

Q: Which coin had the highest compound score?

A: Bitcoin has a max compound score of 0.06908 while for Ethereum it is 0.06956, thus the highest compound score is for Ethereum.

Q. Which coin had the highest positive score?

A: Bitcoin has a max positive score of 0.178 while for Ethereum it is 0.190, thus the highest compound score is for Ethereum.

Discussion: This implies ingeneral the sentiment for Bitcoin on average is better. Likely this is becasue Bitcoin is bigger buzzword compared to Ethereum. It is however intersting to see Bitcoin average negative setiment is significantly higher than that of Ethereum. Likely due to swings for Bitcoin is much higher than Ethereum. Standard deviation of this negative mean is also significantly high for Bitcoin as expected compared to Ethereum.

#### Part 2. Natural Language Processing
1. The text contents data stored on the dataframes were then processed via Regex (to remove special letters/symbols), ran on lemmatizer (to lemmatize), tokenized (sperated to words), stopwords were removed,  converted to lower case, and removed punctuation.    
2. Per article these tokens were put into list of tokens.
3. The token lists corresponding to each article were then added as a column to the dataframe.
4. The column was extracted as list of lists and then converted to a single concatenated list to have the full collection of tokens for all the articles.
5. Ngram (N=2, i.e. bigrams) and frequency analysis was performed on each of these two sets (for Bitcoin and Ethereum). 
6. Top 10 words (considering the frequency) were obtained for each set.
7. Word Clouds were created for each case.
8. Named Entity Recognition (NER) was performed for each case. NER pallette was displayed.
9. A list of entities found was shown as an output. 

### Inputs
Data were read from NEWS Api for both crypto currenciew. Then these textual files were stored in a dataframe. 

### Outputs
Outputs are given out as mentioned above on the terminal as calculated values, visuals (Word Clouds, NERS), and explanations about the results. 

### Remarks
NEWS Api doen not provide a fulltext copy of the articles and after about 300 characters the rest is congeted to show [char +2576] to show the net char value of the rest of texts. Thus the analysis was based on what was extracted under the terms of free use keys obtained. However the code should work if the full texts were provided appropriately. 


