



```python
import nltk
from nltk.corpus import stopwords
nltk.download('stopwords')

# Sample text
text = "This is an example sentence with some stop words that we want to remove."

# Tokenize the text into words
words = nltk.word_tokenize(text)

# Get a list of English stop words
stop_words = set(stopwords.words('english'))

# Remove stop words from the tokenized text
filtered_words = [word for word in words if word.lower() not in stop_words]

# Join the filtered words back into a sentence
filtered_text = ' '.join(filtered_words)

print("Original Text:")
print(text)
print("\nText after Stop Word Removal:")
print(filtered_text)
```