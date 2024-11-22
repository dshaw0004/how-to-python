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

- How to broadcast to all connected clients except sender with python flask socketio ?

```

@socketio.on('receiveMsg')
def text(message, room):
    emit('sendMsg', {'message': message}, broadcast=True, include_self=False, to=room)

```

---

- How to check if all the elements of a list is truthy ?

```

truthy_list = [ 1, 1.3, True, 'wasd']
not_truthy_list = [1, 0, True, 'wasd']

print(f'is truthy_list all truthy ? {all(truthy_list)}') # is truthy_list all truthy ? True
print(f'is not_truthy_list all truthy ? {all(not_truthy_list)}') # is not_truthy_list all truthy ? False

```

---

- How to check if any the elements of a list is truthy ?

```

truthy_list = [ 0, False, 'd']
not_truthy_list = [ 0, False, '']

print(f'does truthy_list have any truthy ? {any(truthy_list)}') # is truthy_list all truthy ? True
print(f'does not_truthy_list have any truthy ? {any(not_truthy_list)}') # is not_truthy_list all truthy ? False

```

---


