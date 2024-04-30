# NATURAL LANGUAGE PROCESSING - QUORA SINCERE AND INSINCERE QUESTIONS FILTERING.

## Data
  https://www.kaggle.com/c/quorainsincere-questions-classification/data

![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/716fd3c3-bd6e-4010-903d-ad32afbc5f5e)
We conducted an analysis of the data, which involved various tasks such asdetermining the length of the longest token and character, identifying the data line containing this token, and calculating several metrics for each data item, including token
count, character length, unique tokens, and the number of special characters and digits present.
Based on our analysis, it has been observed that insincere questions have a greater count of tokens and character length compared to sincere questions. Furthermore,insincere questions also exhibit a higher number of unique tokens when compared to
sincere questions.

![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/50238409-991e-43d8-a53a-84c45bf8a8ef)

![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/3d8fbad3-a693-49b2-bbb3-f0dfa9526491)

![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/3862a3d1-9232-49d3-9f98-274a2758409a)

## Data Processing
1.The process involves changing all the letters in the alphabet to lowercase format, forinstance, changing the word "Word" to "word."
2. A pre-established dictionary of contractions is utilized to expand contractions, such asreplacing "shouldn't" with "should not."
3. We will utilize a special-character dictionary map that has been predefined to eliminate non-English language characters from the text and to insert spaces aroundpunctuation and special characters. For instance, "well, resumé" will be changed to "well , resume," and an exponent such as "2" will be converted to "2."
4. We will correct the 50 most frequent misspellings in the dataset by compiling a list of words that do not appear in the embeddings. As an example, "qoura" will be replaced with "quora."
5. We removed all emojis present in the dataset. Emojis were removed to ensure that the model trained on the dataset would not be biased towards the presence or absence of emojis. To achieve this, we used a regular expression to match all emojis and replaced them with an empty string.
6. We removed all punctuations from the text data. Punctuations were removed as they are typically not useful for text analysis and machine learning models. To remove punctuations, we used the string.punctuation method from the Python string library.
7. The last preprocessing task involved removing all mathematical equations present in the text data. The equations were removed as they do not provide any meaningfulinformation for text analysis. To remove the equations, we used a regular expression to match all text enclosed within [math] and [\math] tags and replaced it with an empty string

## Modeling

### TFIDF with Logistic Refression
![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/9caeab32-7f0f-41d2-b3ff-d5bbde297ded)

### BI-LSTM
![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/8e6d45c0-911c-454b-9b85-e24d78d5da45)

### BERT
![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/9ce8b869-af03-4895-a6e8-01ad93c1cf17)


