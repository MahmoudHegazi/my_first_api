# my_first_api
Advanced API with good syntax 


```python
import string
import random


#my keygen
lower_letters = string.ascii_lowercase
upper_letters = string.ascii_uppercase
ints = [0,1,2,3,4,5,6,7,8,9]
kind_chars = ['@','_','-','~']

def key_gen(size):
    speacial = random.choice(kind_chars)
    key = speacial
    for repeat in range(size):
        randomize = ''
        lower_char = str(random.choice(lower_letters))
        upper_char = str(random.choice(upper_letters))
        number = str(random.choice(ints))
        lis = [lower_char, upper_char, number]
        first = lis[random.choice([0,1,2])]
        second = lis[random.choice([1,2,0])]
        third = lis[random.choice([1,0,2])]
        randomize = second + first + third
        
        key += randomize
    speacial = random.choice(kind_chars)
    key += speacial
        
    print(key)
    
key_gen(20)

```
