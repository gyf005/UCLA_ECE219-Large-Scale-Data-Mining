Some of the notebooks for the second task (i.e. Twitter data) will not run fully as is. Here are some instructions:

Q1 - Q8: Project4.ipynb

Q9 + Part 1: Predicting the supported team based on content

This file, named "Part_1.ipynb" found in the parent directory (also contains code for Question 9), was run locally with data found in path
"ECE219_tweet_data/tweets_#{tweetgroup}.txt" as shown in the first few blocks. The import and extraction of data takes approx ~10 minutes,
so we save the file as a CSV and download for repeated use. Skip these 'df.to_csv' and 'df = pd.read_csv' code blocks to use the extracted
data without saving and importing. Everything else can be run as is.

Part 2: Predicting number of likes based on content and sentiment

This file was run on Colab with data uploaded to Google Drive as shown in the first few code blocks. The import and extraction of data takes approx ~30 minutes,
so we save the file as a CSV and download for repeated use. Skip these 'df.to_csv' and 'df = pd.read_csv' code blocks to use the extracted data without saving and
importing. Everything else can be run as is, however, it will take ~1.5 hours to run the whole notebook.

Part 3: Predicting relative time using GLoVE embeddings

This file was run on Colab with data uploaded to Google Drive as shown in the first few code blocks. The import and extraction of data takes approx ~60 minutes,
so we save the file as a CSV and download for repeated use. Skip these 'df.to_csv' and 'df = pd.read_csv' code blocks to use the extracted data without saving and
importing. Some local processing is required for this notebook. In the 8th code block, we write the Twitter text to 'drive/MyDrive/Twitter/tweets_text_nfl_1.txt'.
Locally, we run the script: https://nlp.stanford.edu/projects/glove/preprocess-twitter.rb, piping the 'tweets_text_nfl_1.txt' file into the Ruby program, and creating
the output 'cleaned_tweets_1.txt'. This is imported into the Google Colab notebook and represents the cleaned text based on GLoVE Twitter preprocessing.

Later in the notebook, we import GLoVE embeddings from file: 'drive/MyDrive/Twitter/glove.twitter.27B.100d.txt', which can be found here:
https://nlp.stanford.edu/projects/glove/. However, the GLoVE file doesn't represent a word2vec format, so we need to add '1193514, 100' to the first line of the file
before uploading to Drive and importing in the notebook. Everything else can be run as is, however, it will take ~3 hours to run the whole notebook.
