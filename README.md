# text-processing
import nltk
from nltk.tokenize import word_tokenize
from nltk.tokenize import sent_tokenize
nltk.download('punkt_tab')
from nltk.corpus import stopwords
nltk.download('stopwords')
text="Hey, can u plz tell me where’s my order??”.“i didn’t receive my parcel yet!!!!”.“Whr’s my ordr 😡😡”.“delivery late af... i want refund now"
## lowearcase
text_lower=text.lower()
print("Lowearcase:",text_lower)
## wordTokenize
wt=word_tokenize(text)
print("Word_Tokenize:",wt)
# sentenceTokenize
st=sent_tokenize(text)
print("sentence_Tokenize:",st)
## punctuation remove
import re
import nltk
from nltk.tokenize import word_tokenize

url_pattern = r'http[s]?://(?:[a-zA-Z]|[0-9]|[$-_@.&+]|[!*\\(\\),]|(?:%[0-9a-fA-F][0-9a-fA-F]))+'
punctuation_pattern = r'[^\w\s]'

text = re.sub(url_pattern, '', text)
text = re.sub(punctuation_pattern, ' ', text)

tokens = word_tokenize(text)

print(tokens)
print(text)
#stopword removing

tokens=word_tokenize(text)

stop_words=set(stopwords.words('english'))

filtered_tokens=[word for word in tokens if word.lower() not in stop_words]

filtered_sentence=' '.join(filtered_tokens)
print("Sentence original:",text)
print(filtered_sentence)
## whitespace
from nltk.tokenize import WhitespaceTokenizer
ws = WhitespaceTokenizer()
wpt = ws.tokenize(text)
   
print(wpt)
