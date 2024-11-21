# How To Python

A gathering of bunch of how to questions and answers for Python Programming Language.

## Let's Start


- How to get path of all the files of a specific type ?

```
import glob
all_md_files = glob.glob('*.<file-extension>')
```

---

- how to convert a csv file into python dictionary

```
import csv

with open('file.csv', 'r') as file:
    reader = csv.DictReader(file)
    data: list[dict] = list(reader)

```

---

- How to sort a list of dictionaries by a value of dictionary

```
new_list = sorted(old_list, key=lambda d: d['date'], reverse=True) 
# reverse=True for descending order else it will sort in ascending order
```

---

- How to get sibling elements in BeautifulSoup ?

```
from bs4 import BeautifulSoup

soup = BeautifulSoup(content, 'html.parser')

element = soup.find('div', attrs={'class': 'important-element'})
next_element = element.find_next('div', attrs={'class': 'next'})
previous_element = element.find_previous('div', attrs={'class': 'previous'})
```

---

