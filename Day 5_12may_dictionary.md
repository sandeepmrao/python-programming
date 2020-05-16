# Dictionary
key:value pairs


```python
#empty dictionary:
d={}
print(type(d))
```

    <class 'dict'>
    


```python
d={'name':'ram','age':25,'gender':"male",'covid':"-ve"}
print(d)
```

    {'name': 'ram', 'age': 25, 'gender': 'male', 'covid': '-ve'}
    


```python
len(d)
```




    4




```python
#access element thru key:
d['age']
```




    25




```python
#tuples as key :
d1={(1,2):'combo1',(3,4):'combo2'}
print(d1)
```

    {(1, 2): 'combo1', (3, 4): 'combo2'}
    

## note: keys are immutable and so dict. must have immuatble keys, so list cannot be used as keys


```python
d2={'A':10,'B':9,'C':8,'E':6}
d2['D']=7 #add element to dict.
print(d2)
```

    {'A': 10, 'B': 9, 'C': 8, 'E': 6, 'D': 7}
    


```python
#delete elemnt:
del d2['E']
print(d2)
```

    {'A': 10, 'B': 9, 'C': 8, 'D': 7}
    


```python
d2.pop('C')
print(d2)
d1.popitem()
print(d1)
```

    {'A': 10, 'B': 9, 'D': 7}
    {(1, 2): 'combo1'}
    


```python
d2.items()

```




    dict_items([('A', 10), ('B', 9), ('D', 7)])




```python
d2.keys()
```




    dict_keys(['A', 'B', 'D'])




```python
d2.values()
```




    dict_values([10, 9, 7])




```python
d2.update()
```


```python
print(d2)
```

    {'A': 10, 'B': 9, 'D': 7}
    


```python
#copy dictionary:
d3=d2.copy()
print(d3)
```

    {'A': 10, 'B': 9, 'D': 7}
    


```python
d2['C']=8
d3.update()
print(d3)
```

    {'A': 10, 'B': 9, 'D': 7}
    


```python
for i in d2:
    dx=d2.keys()>8
    print(i)
print(dx)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-18-adcb5265831b> in <module>
          1 for i in d2:
    ----> 2     dx=d2.keys()>8
          3     print(i)
          4 print(dx)
    

    TypeError: '>' not supported between instances of 'dict_keys' and 'int'



```python
for i in d.items():
    print(i,end=' ')
```

    ('name', 'ram') ('age', 25) ('gender', 'male') ('covid', '-ve') 


```python
## dict. comprehensions
dz={i:i**3 for i in range(1,5)}
print(dz)
```

    {1: 1, 2: 8, 3: 27, 4: 64}
    


```python
#input dict. using comprehensions
n=range(1,8)
day=['sun','mon','tue','wed','thurs','fri','sat','sun']
week={i:j for (i,j) in zip(n,day)}
print(week)
```

    {1: 'sun', 2: 'mon', 3: 'tue', 4: 'wed', 5: 'thurs', 6: 'fri', 7: 'sat'}
    


```python
da={1:10,2:20}
db={3:30,4:50}
da.update(db)
print(da)
```

    {1: 10, 2: 20, 3: 30, 4: 50}
    


```python
d.setdefault('age',16)
```




    25




```python
d.setdefault('city','new delhi')
print(d)
```

    {'name': 'ram', 'age': 25, 'gender': 'male', 'covid': '-ve', 'city': 'new delhi'}
    


```python
#create dict. from fromkeys:
ds=dict.fromkeys(n,'val')
print(ds)
```

    {1: 'val', 2: 'val', 3: 'val', 4: 'val', 5: 'val', 6: 'val', 7: 'val'}
    


```python
l1=list(d.items())
print(l1)
```

    [('name', 'ram'), ('age', 25), ('gender', 'male'), ('covid', '-ve'), ('city', 'new delhi')]
    

### Functions:part 2:


```python
#fn for fibonnoci series:
def fib_ser(n):
    i1=0
    i2=1
    sum=0
    print('the series is: ')
    for i in range(n):
        print(i1,end=' ')
        sum=i1+i2
        i1=i2
        i2=sum
        
```


```python
fib_ser(11)
```

    the series is: 
    0 1 1 2 3 5 8 13 21 34 55 

### lambda functions:


```python
x=lambda para1:para1*para1
```


```python
x(12)
```




    144




```python
import math
dist=lambda p1,p2:math.sqrt(p1**2+p2**2) # p1 &p2 are formal parameters
```


```python
dist(10,20) #actual parameters
```




    22.360679774997898




```python
dist(p2=10,p1=20) #positional parameters
```




    22.360679774997898




```python
#fn to get bits: dec to nay base no.- the bits shd be inserted from last to first
def convert(n,base):
    t=n
    lst=[]
    while t>0:
        bit=t%base
        lst.insert(0,bit) #insert at 0th index
        t//=base
    return(lst)
```


```python
bn=convert(10,2)
print(bn)
```

    [1, 0, 1, 0]
    


```python
oct=convert(10,8)
print(oct)
```

    [1, 2]
    


```python
#default parameters in a function
def convert1(n,base=2):
    t=n
    lst=[]
    while t>0:
        bit=t%base
        lst.insert(0,bit) #insert at 0th index
        t//=base
    return(lst)
```


```python
#call above fn with a default value
bn1=convert1(10) #by default it has taken base=2
print(bn1)
```

    [1, 0, 1, 0]
    


```python
oct1=convert1(10,8)
print(oct1)
```

    [1, 2]
    

### types of variables:


```python
# s is passed by value, i.e even if s is changed inside fn, 
#it is not reflected outside the fn, immutable objects cannot be changed outside the fn
# immutable objects are passed by value, like strings, tuples,etc
def pas_val(s):     #s is a parameter
    s1='hi'         #s1 is local var
    s+=s1
    print('m inside fn',s)
```


```python
x='hello'
pas_val(x)
print('m outside fn',x)
```

    m inside fn hellohi
    m outside fn hello
    


```python
# pass by refernce, all mutable objects are passed by referance
#changes made inside fn is reflected outside the fn
def pas_ref(l):
    l.append(100)
    print('m inside fn l= ',l)
```


```python
x=[5,10,15]
pas_ref(x)
print('m outside fn x: ',x)
```

    m inside fn l=  [5, 10, 15, 100]
    m outside fn x:  [5, 10, 15, 100]
    


```python

```
