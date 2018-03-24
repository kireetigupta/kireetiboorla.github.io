---
layout: post
title: Text Pre-processing
---
## Accessing Text
1. #### From Web
```python
from urllib import request
url = "http://www.gutenberg.org/files/2554/2554.txt"
response = request.urlopen(url)
raw = response.read().decode('utf8')
```




### References
1.[http://www.nltk.org/book/ch03.html](NLTK Org book)
