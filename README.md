**Keywords with NLP**

Project uses the NIPS (*Neural Information Processing Systems*) Papers. The files used can be found on the following URL:  [NIPS Papers](https://www.kaggle.com/benhamner/nips-papers/home)

  In this project I am using NLP (*Natural Language Processing*) to extract keywords from the Abstract of a document. This is completed using a series of different steps including a scoring system in conjunction with NLP. First, I correctly prepared the data by first loading the papers.csv document, then extracting the “Abstract” data into a data frame, allowing for better analysis. I also found the word count just to get a better understanding of which words are used the most.

  I began to pre-process the text by taking the text found in the abstract columns, and adding each word to a corpus, which is just a structured set of text. This corpus contains words that do not include punctuation, special characters, or digits. It was also “Lemmitized” and “Stemmered”, which essentially turns each word into its basic form, allowing for a cleaner analysis.

  I continued by visualizing this data, first by simply visualizing the corpus with a Word Cloud visualization. I then expanded this visualization by creating plots for frequently used uni-grams (one word), bi-grams (two words), and tri-grams (three words). To do this I created a vector of word counts to build a vocabulary of known words. I made sure to take out words that having a frequency higher than a specific threshold (in this case 0.8), to ensure that I only have words relevant to the context and not commonly used words. 
  ![Word Cloud](https://github.com/slarionne/NLP-Keyword-Extraction-from-Articles/blob/master/word1.png)

  After visualizing I began the steps towards converting this to a matrix of integers. To do this I refined the word counts using the TF-IDF vectorizer which scales down the impact of tokens that occur very frequently in a corpus. These tokens are less informative than features that occur in a small fraction of the training corpus. Finally, these vocabulary words are sorted and scored based on the previous mentioned features. The top vocabulary words are then mentioned below with the score stated next to those words.

