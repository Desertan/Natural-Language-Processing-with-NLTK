# Natural-Language-Processing-with-NLTK
 Example processing text using the NLTK library.
import nltk
from nltk.tokenize import word_tokenize
from nltk.corpus import stopwords
from nltk.probability import FreqDist

nltk.download('punkt')
nltk.download('stopwords')

# Sample text for processing
text = "Natural Language Processing is a subfield of artificial intelligence that focuses on the interaction between computers and humans using natural language."

# Tokenize the text
tokens = word_tokenize(text)

# Remove stop words
stop_words = set(stopwords.words('english'))
filtered_tokens = [word for word in tokens if word.lower() not in stop_words]

# Calculate word frequencies
freq_dist = FreqDist(filtered_tokens)
print(freq_dist.most_common(5))
