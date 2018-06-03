# Sentimental-Analysis-based-on-Opinion-Target-and-Opinion-word-mining.
This project aim to target sentiment analysis based on opinion words (like good, bad, beautiful, wrong, best, awesome, etc) of selected opinion target ( like product name for amazon product reviews). The code provides steps of pre-processing like stopword removal, removal of duplicates in the review, spelling correction, etc. From the review biwords and triwords are generated for each reviewed text and use it to generate 8 patterns from rule-based method (by POS tagging). Opinion target and their opinion words are extracted using these 8 patterns. The extracted opinion words gets polarity directly from TextBlob library using polarity function of sentiment class. This polarity is generated for every opinion word in every reviewed text, and the highest magnitude polarity word is selected from every reviewed text. These highest magnitude polarity word along with its polarity is selected in a list named tuple_word_score.  These list is used for searching focused opinion words and eliminate noise within the data. Afterword the average of all the polarity of opinion word is taken and decide a threshold to categories positive and negative semantics. Whole project used semi-supervised approach wherein predefined list of opinion target was provided in a variable named stuff. The synonyms of these opinion targets are used to figure out many opinion words within the pattern. In addition, synonyms of opinion words are also included in the opinion word set to the generated similar opinion words of the pattern.
