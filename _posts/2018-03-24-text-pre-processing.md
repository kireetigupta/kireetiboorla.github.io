---
layout: post
title: Text Pre-processing
category: concepts
---

#### Getting text from Web
```python
from urllib import request
url = "http://www.gutenberg.org/files/2554/2554.txt"
response = request.urlopen(url)
raw = response.read().decode('utf8')
```
#### Dealing with HTML
We will use beautifulSoup to do this. Learn as much as you can here.
#### Getting raw content from HTML page.
```python
from bs4 import BeautifulSoup
raw=BeautifulSoup(response).get_text()
toekns=word_tokenize(raw) # from  nltk import word_tokenize
```
** Summarize the below resources and do a poc. **
1.[Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-scrape-web-pages-with-beautiful-soup-and-python-3)
2.[Stanford Tut](http://web.stanford.edu/~zlotnick/TextAsData/Web_Scraping_with_Beautiful_Soup.html)


### Processing search engine results.
Search engines do present certain difficulties like
1. Inconsistent results for the same query based on time, location.
2. Change in the output pattern.
3. Limited search capabilities in terms of regex.

### Reading local files.
1.use open("filepath") to open file
2. use read/readLines() to read.
```python
with open("file") as f:
  lines=f.read().splitlines() # or lines = f.readlines()
  for x in lines:# or f:
    print(x)
```
### Text Processing With Unicode




### References
1.[http://www.nltk.org/book/ch03.html](NLTK Org book)
