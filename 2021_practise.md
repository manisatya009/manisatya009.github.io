```python
s=('eigoEKFNEIIueoneuhuhouh')
```


```python
m=s.lower()
```


```python
print(m)
```


```python
print(m.count('e'))
```


```python
m=m.replace('e','io')
```


```python
print(m)
```


```python
s = input('Enter a string')
if s[0].isalpha():
    print('Your string starts with a letter')
for i in range(len(s)):
    if not s[i].isalpha():
        print('Your string contains a non-letter.')
```


```python
s = input('Enter a string')
for i in range(len(s)):
    print(s[i].isaplha())
```


```python
print('\n qe'*9)
```


```python
L = eval(input('Enter a list: '))
for i in range(len(L)):
    print('The  element is ', L[i])
```

    Enter a list: 234,'e3r3r'
    The  element is  234
    The  element is  e3r3r
    


```python
for i in range(2):
    print (i)
```

    0
    1
    


```python
from random import sample
names = ['Joe', 'Bob', 'Sue', 'Sally']
team = sample(names, 2)

```


```python
team
```




    ['Sue', 'Bob']




```python
list('abi3344')
```




    ['a', 'b', 'i', '3', '3', '4', '4']




```python
for i in range(1,11):
    for j in range(1,11):
        print('{:5d}'.format(i*j), end=' ')
    print()
```

        1     2     3     4     5     6     7     8     9    10 
        2     4     6     8    10    12    14    16    18    20 
        3     6     9    12    15    18    21    24    27    30 
        4     8    12    16    20    24    28    32    36    40 
        5    10    15    20    25    30    35    40    45    50 
        6    12    18    24    30    36    42    48    54    60 
        7    14    21    28    35    42    49    56    63    70 
        8    16    24    32    40    48    56    64    72    80 
        9    18    27    36    45    54    63    72    81    90 
       10    20    30    40    50    60    70    80    90   100 
    


```python
d = {'A':100, 'B':200}
```


```python
d
```




    {'A': 100, 'B': 200}




```python
d['A']
```




    100




```python
d = {'A':100, 'B':200}
```


```python
points = {'A':1, 'B':3, 'C':3, 'D':2, 'E':1, 'F':4, 'G':2,
'H':4, 'I':1, 'J':8, 'K':5, 'L':1, 'M':3, 'N':1,
'O':1, 'P':3, 'Q':10, 'R':1, 'S':1, 'T':1, 'U':1,
'V':4, 'W':4, 'X':8, 'Y':4, 'Z':10}
```


```python
points
```




    {'A': 1,
     'B': 3,
     'C': 3,
     'D': 2,
     'E': 1,
     'F': 4,
     'G': 2,
     'H': 4,
     'I': 1,
     'J': 8,
     'K': 5,
     'L': 1,
     'M': 3,
     'N': 1,
     'O': 1,
     'P': 3,
     'Q': 10,
     'R': 1,
     'S': 1,
     'T': 1,
     'U': 1,
     'V': 4,
     'W': 4,
     'X': 8,
     'Y': 4,
     'Z': 10}




```python
score=sum([points[c] for c in word])
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-11-7764a34497e4> in <module>
    ----> 1 score=sum([points[c] for c in word])
    

    NameError: name 'word' is not defined



```python
list(d)
```




    ['A', 'B']




```python
def convert(t):
    return t*9/5+32
print(convert(20))
```

    68.0
    


```python
d = {'dog' : 'has a tail and goes woof!',
'cat' : 'says meow',
'mouse' : 'chased by cats'}

```


```python
word = input('Enter a word: ')
print('The definition is:', d[word])

```

    Enter a word: mouse
    The definition is: chased by cats
    


```python
points = {'A':1, 'B':3, 'C':3, 'D':2, 'E':1, 'F':4, 'G':2,
'H':4, 'I':1, 'J':8, 'K':5, 'L':1, 'M':3, 'N':1,
'O':1, 'P':3, 'Q':10, 'R':1, 'S':1, 'T':1, 'U':1,
'V':4, 'W':4, 'X':8, 'Y':4, 'Z':10}
```


```python

import numpy as np
import pandas as pd


import os
```


```python
text = open('C://Users//madi//Desktop//mltxtpractise.txt').read()
```


```python
text
```




    'I am manikanta maddimsetti, i am jeigeijge aneigheg kniegie.\nakengieg \ndijieg,ekfheuhgiege,ajguehgijeg,dneiughiejgem,\nneigjiegn\nI am good at playing games.'




```python
from string import punctuation
text = text.lower()
for p in punctuation:
    text = text.replace(p, '')


```


```python
text
```




    'i am manikanta maddimsetti i am jeigeijge aneigheg kniegie\nakengieg \ndijiegekfheuhgiegeajguehgijegdneiughiejgem\nneigjiegn\ni am good at playing games'




```python
words=text.split()
```


```python
words
```




    ['i',
     'am',
     'manikanta',
     'maddimsetti',
     'i',
     'am',
     'jeigeijge',
     'aneigheg',
     'kniegie',
     'akengieg',
     'dijiegekfheuhgiegeajguehgijegdneiughiejgem',
     'neigjiegn',
     'i',
     'am',
     'good',
     'at',
     'playing',
     'games']




```python
d = {}
for w in words:
    if w in d:
        d[w] = d[w] + 1
    else:
        d[w] = 1

```


```python
d
```




    {'i': 3,
     'am': 3,
     'manikanta': 1,
     'maddimsetti': 1,
     'jeigeijge': 1,
     'aneigheg': 1,
     'kniegie': 1,
     'akengieg': 1,
     'dijiegekfheuhgiegeajguehgijegdneiughiejgem': 1,
     'neigjiegn': 1,
     'good': 1,
     'at': 1,
     'playing': 1,
     'games': 1}




```python
d['king']=1
```


```python
d
```




    {'i': 3,
     'am': 3,
     'manikanta': 1,
     'maddimsetti': 1,
     'jeigeijge': 1,
     'aneigheg': 1,
     'kniegie': 1,
     'akengieg': 1,
     'dijiegekfheuhgiegeajguehgijegdneiughiejgem': 1,
     'neigjiegn': 1,
     'good': 1,
     'at': 1,
     'playing': 1,
     'games': 1,
     'king': 1}




```python
l=list(d.values())
```


```python
l
```




    [3, 3, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]




```python
l=list(d)
```


```python

```


```python
l
```




    ['i',
     'am',
     'manikanta',
     'maddimsetti',
     'jeigeijge',
     'aneigheg',
     'kniegie',
     'akengieg',
     'dijiegekfheuhgiegeajguehgijegdneiughiejgem',
     'neigjiegn',
     'good',
     'at',
     'playing',
     'games',
     'king']




```python
set([1,4,4,4,5,1,2,1,3])
set('this is a test')

```




    {' ', 'a', 'e', 'h', 'i', 's', 't'}



# importing files


```python
import os

```


```python
os.getcwd
```




    <function nt.getcwd()>




```python
os.chdir('C:/Users/madi/Desktop')
```


```python
import os
directory = 'C:/Users/madi/Desktop'
files = os.listdir(directory)

```


```python
files
```




    ['cimpress',
     'desk2021',
     'desktop.ini',
     'ee.txt',
     'interview Prep',
     'Manikanta_Maddimsetti.docx',
     'mltxtpractise.txt',
     'New Microsoft Excel Worksheet.xlsx',
     'New Microsoft Word Document.docx',
     'New Text Document (2).txt',
     'New Text Document.txt',
     'SeagateToolkit.exe',
     'Tor Browser',
     '~$i machine learning data.docx',
     '~$Incredibles (1).xlsx',
     '~$New Microsoft Excel Worksheet (2).xlsx',
     '~$w Microsoft Word Document.docx']




```python
tup=tuple('string')
```


```python
tup
```




    ('s', 't', 'r', 'i', 'n', 'g')




```python
tup=tuple([['foo','ist'],'string',True])
```


```python
tup=tuple([[1,2],'string',True])
```


```python
tup = tuple(['foo', [1, 2], True])
```


```python
tup[1].append('tow')
```


```python
tup
```




    ('foo', [1, 2, 4, 'tow'], True)




```python
tup1=([1,2,4])
```


```python
tup11=tup1*2
```


```python
tup11
```




    [1, 4, 4, 1, 4, 4]




```python
for i in tup11:
    tup11[i]=tup11[i]*2
```


    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    <ipython-input-53-d5630fc9c9c7> in <module>
          1 for i in tup11:
    ----> 2     tup11[i]=tup11[i]*2
    

    IndexError: list index out of range



```python
tup11
```




    [1, 4, 4, 1, 4, 4]




```python
l=list(tup11)
```


```python
l
```




    [1, 8, 4, 1, 4, 4]




```python
l.insert(2,'win')
```


```python
l

```




    [1, 8, 'win', 4, 1, 4, 4]




```python
l.extend(tup11)
```


```python
l

```




    [1, 8, 'win', 4, 1, 4, 4, 1, 8, 4, 1, 4, 4]




```python
c=[]
for i in l:
    c.extend(i)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-62-413304c551c2> in <module>
          1 c=[]
          2 for i in l:
    ----> 3     c.extend(i)
    

    TypeError: 'int' object is not iterable



```python
 words = ['apple', 'bat', 'bar', 'atom', 'book']

```


```python
by_letter = {}
```


```python
for word in words:
    letter = word[0]
    if letter not in by_letter:
        by_letter[letter] = [word]
    else:
        by_letter[letter].append(word)

```


```python
by_letter
```




    {'a': ['apple', 'atom'], 'b': ['bat', 'bar', 'book']}




```python
for word in words:
    letter = word[0]
    by_letter.setdefault(letter, []).append(word)

```


```python
strings = ['a', 'as', 'bat', 'car', 'dove', 'python']

```


```python
 [x for x in strings if len(x)>3]
```




    ['dove', 'python']




```python
all_data = [['John', 'Emily', 'Michael', 'Mary', 'Steven'],
 ['Maria', 'Juan', 'Javier', 'Natalia', 'Pilar']]
```


```python
all_data
```




    [['John', 'Emily', 'Michael', 'Mary', 'Steven'],
     ['Maria', 'Juan', 'Javier', 'Natalia', 'Pilar']]




```python
names_of_interest = []
for names in all_data:
    enough_es = [name for name in names if name.count('e') >= 2]
    names_of_interest.extend(enough_es)

```


```python
names_of_interest
```




    ['Steven']




```python
a=[]
def mylol(x,y,z=1.5):
    if z > 1:
        return z * (x + y)
    else:
        return z / (x + y)


```


```python
mylol(5,6)
```




    16.5



# map function


```python
 states = [' Alabama ', 'Georgia!', 'Georgia', 'georgia', 'FlOrIda',
'south carolina##', 'West virginia?']

```


```python
states
```




    [' Alabama ',
     'Georgia!',
     'Georgia',
     'georgia',
     'FlOrIda',
     'south carolina##',
     'West virginia?']




```python
def remove_punctuation(value):
    return re.sub('[!#?]', '', value)
import re
```


```python
for x in map(remove_punctuation, states):
    print(x)
```

     Alabama 
    Georgia
    Georgia
    georgia
    FlOrIda
    south carolina
    West virginia
    


```python

```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-98-f920e8389072> in <module>
          1 ints = [4, 0, 1, 5, 6]
    ----> 2 apply_to_list(ints, lambda x: x * 2)
    

    NameError: name 'apply_to_list' is not defined


# used for lambda function



```python
def apply_to_list(some_list, f):
    return [f(x) for x in some_list]
```


```python
ints = [4, 0, 1, 5, 6]
apply_to_list(ints, lambda x: x * 2)

```




    [8, 0, 2, 10, 12]



# ARRAYS


```python
data1 = [6, 7.5, 8, 0, 1]
```


```python
arr1=np.array(data1)
```


```python
arr1
```




    array([6. , 7.5, 8. , 0. , 1. ])




```python
arr2d = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

```


```python
arr2d[2,2]
```




    9




```python
arr=np.arange(24).reshape(2,3,4)
```


```python
arr
```




    array([[[ 0,  1,  2,  3],
            [ 4,  5,  6,  7],
            [ 8,  9, 10, 11]],
    
           [[12, 13, 14, 15],
            [16, 17, 18, 19],
            [20, 21, 22, 23]]])




```python
arr[0]
```




    array([[ 0,  1,  2,  3],
           [ 4,  5,  6,  7],
           [ 8,  9, 10, 11]])




```python
arr[1]
```




    array([[12, 13, 14, 15],
           [16, 17, 18, 19],
           [20, 21, 22, 23]])




```python
arr[0]+arr[1]
```




    array([[12, 14, 16, 18],
           [20, 22, 24, 26],
           [28, 30, 32, 34]])




```python
arr[0][0]+arr[0][1]+arr[0][2]+arr[1][0]+arr[1][1]+arr[1][2]
```




    array([60, 66, 72, 78])




```python

```

# Pandas


```python
import pandas as pd
```


```python
from pandas import Series,DataFrame
```


```python
obj = pd.Series([4, 7, -5, 3])
```


```python
obj
```




    0    4
    1    7
    2   -5
    3    3
    dtype: int64




```python
obj2 = pd.Series([4, 7, -5, 3], index=['d', 'b', 'a', 'c'])
```


```python
obj2
```




    d    4
    b    7
    a   -5
    c    3
    dtype: int64




```python
obj2[['d','c']]
```




    d    4
    c    3
    dtype: int64



# to select more than one element in pandads we need to use []


```python
obj2['a']
```




    -5




```python
obj2[obj2>3]
```




    d    4
    b    7
    dtype: int64




```python
sdata = {'Ohio': 35000, 'Texas': 71000, 'Oregon': 16000, 'Utah': 5000}

```


```python
obj3=pd.Series(sdata)
```


```python
obj3
```




    Ohio      35000
    Texas     71000
    Oregon    16000
    Utah       5000
    dtype: int64




```python
 states = ['California', 'Ohio', 'Oregon', 'Texas']
```


```python
obj=pd.Series(sdata,index=states)
```


```python
obj
```




    California        NaN
    Ohio          35000.0
    Oregon        16000.0
    Texas         71000.0
    dtype: float64




```python

```
