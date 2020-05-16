# sets and tuples

## sets
elemnts are unorders and no duplicates 


```python
s1={2,5,7,9,10,5,2,7,23}
print(type(s1))
print(s1)
```

    <class 'set'>
    {2, 5, 7, 9, 10, 23}
    


```python
#create empty set:
s=set() #empty set
s1={}  #empty dictionary
type(s)
type(s1)
```




    dict




```python
fruits={"apples",'grapes','kiwi','apples'}
print(type(fruits))
print(fruits)
```

    <class 'set'>
    {'apples', 'kiwi', 'grapes'}
    

### operations on sets


```python
#membership testing: in
'kiwi' in fruits
```




    True




```python
'fruit' in fruits
```




    False




```python
# union of two sets: union or |
x={4,8,9,12,16,20,25}
y={10,20,25,12,56,98}
z=x.union(y)
print(z)
print(x|y)
```

    {98, 4, 8, 9, 10, 12, 16, 20, 56, 25}
    {98, 4, 8, 9, 10, 12, 16, 20, 56, 25}
    


```python
a,b={1,2,3,4,5},{4,5,6,7,8,9}
print(a|b)

```

    {1, 2, 3, 4, 5, 6, 7, 8, 9}
    


```python
#intersection: intersection or &
print(x&y)
print(x.intersection(y))
```

    {25, 12, 20}
    {25, 12, 20}
    


```python
# difference: difference or -
print(x-y)
print(x.difference(y))
```

    {8, 9, 4, 16}
    {8, 9, 4, 16}
    


```python
# comparision of sets: == < (proper sunset)  <=>(proper superset)
print(x>y) # y is a subset of x: for proper subset
```

    False
    


```python
a={2,4,6}
b={2,4,8,10,6}
print(b>a)
print(a>b)
```

    True
    False
    


```python
a==b
```




    False




```python
# add an element to a set:
fruits.add('mango')
print(fruits)
```

    {'mango', 'apples', 'kiwi', 'grapes'}
    


```python
fruits.remove('apples')
print(fruits)
```

    {'mango', 'kiwi', 'grapes'}
    

## *set is mutable
list is mutable
string is immuatble


```python
# conversions: list to set:
l1=[2,7,5,6]
s1=set(l1)
print(type(s1))
print(s1)
```

    <class 'set'>
    {2, 5, 6, 7}
    


```python
# conversions:string to set:
st1='good luck'
s1=set(st1)
print(type(s1))
print(s1)
```

    <class 'set'>
    {'o', 'g', 'u', ' ', 'k', 'l', 'd', 'c'}
    


```python
# set comprehension
s2={i for i in [2,20,-3,50]}
print(s2)
```

    {2, 50, 20, -3}
    


```python
s2={i for i in [2,20,-3,50] if i%5==0}
print(s2)
```

    {50, 20}
    


```python
# count vowels in the string
vowels={'a','e','i','o','u'}
count=0
for i in "good morning foodies":
    if i in vowels:
        count+=1
print(count)
```

    8
    

## Functions


```python
#sigmoid function with one parameter and one return value
import math
def sigmoid(z):
    result=1/(1+math.exp(-z))
    return result
```


```python
sigmoid(10)
```




    0.9999546021312976




```python
#fn defination for a list:
def avg(x):
    print(type(x))
    return sum(x)/len(x)
```


```python
a=[5,6,8,12]
print(avg(a))
```

    <class 'list'>
    7.75
    


```python
print(vowels)
```

    {'o', 'i', 'e', 'u', 'a'}
    


```python
#fn defination for a string:
def vowel_count(s):
    count=0
    for i in s:
        if i in vowels:
            count+=1
    return count
```


```python
print(vowel_count('ali baba and 40 chor'))

```

    6
    


```python
#fn to check a prime no.
def prime_check(n):
    for i in range(2,n//2+1):
        if n%i==0:
            return False
        else:
            return True
```


```python
prime_check(23)
```




    True




```python
prime_check(9)
```




    True



## Tuples: 


```python
#tuple uses() or without any type of brackets
t1=(2,0.5,10)
t2=2,0.5,10
print(t1)
print(t2)
```

    (2, 0.5, 10)
    (2, 0.5, 10)
    


```python
t1=10,2.7,'hello','superu'
print(t1)
```

    (10, 2.7, 'hello', 'superu')
    


```python
#indexing & slicing:
t1[2]
```




    'hello'




```python
print(t1[:2])
```

    (10, 2.7)
    

### no insert and delete -->tuples are immutable


```python
t1.index(2.7)
```




    1




```python
#nested tuples
t3=t1,[2,5,7],'hello',10
```


```python
print(t3)
```

    ((10, 2.7, 'hello', 'superu'), [2, 5, 7], 'hello', 10)
    


```python
t3.count('hello')
```




    1




```python
t3.count(10)
```




    1




```python
t3.index('hello')
```




    2




```python
t3[0][2]
```




    'hello'




```python
print(len(t3))
```

    4
    

#### max,min and sum fns are possible on tuples


```python
#sorting tuples:
tx=-5,-20,5,65,12
tx=sorted(tx)
print(tx)
```

    [-20, -5, 5, 12, 65]
    


```python
print(tx[::-1])
```

    [65, 12, 5, -5, -20]
    


```python
#type conversion:
s='hello'
t=tuple(s)
print(t)
```

    ('h', 'e', 'l', 'l', 'o')
    


```python
# use of in operator in tuples:
ty=2,8,9,7,1,5
for i in t:
    print(i*2,end=' ')
for i in ty:
    print(i*2,end=' ')
```

    hh ee ll ll oo 4 16 18 14 2 10 


```python
# un packing
tz='hello',10,True
x,y,z=tz
print(x)
print(y)
print(z)
```

    hello
    10
    True
    


```python
#ennumareation: assigning a numeric value to each elemet
fruits='apple','kiwi','mango'
t=enumerate(fruits,3) #starts from 3 w.r.t element in fruits
print(type(t))
t=tuple(t)
print(t)
```

    <class 'enumerate'>
    ((3, 'apple'), (4, 'kiwi'), (5, 'mango'))
    


```python
#ennumerate and un-packing
wk='mon','tue','wed','thurs','fri','sat','sun'
tw=enumerate(wk,1)
tw=tuple(tw)
print(tw)
for x,y in tw:
    print(x,y)
```

    ((1, 'mon'), (2, 'tue'), (3, 'wed'), (4, 'thurs'), (5, 'fri'), (6, 'sat'), (7, 'sun'))
    1 mon
    2 tue
    3 wed
    4 thurs
    5 fri
    6 sat
    7 sun
    


```python
#zip;
cgpa=5.5,6.3,7.8,8.9,9.2
grades='D','C','B','A','A+'
result=zip(cgpa,grades)
print(result)
for i,j in result:
    print(i,':',j)
```

    <zip object at 0x000000E355BECEC8>
    5.5 : D
    6.3 : C
    7.8 : B
    8.9 : A
    9.2 : A+
    


```python
result=list(result)
print(result)
```

    []
    


```python

```
