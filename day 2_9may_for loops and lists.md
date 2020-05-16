## Sequence data type: 

1.range()


```python
x=list(range(5))
```


```python
print(x)
```

    [0, 1, 2, 3, 4]
    


```python
for i in range(5):
    print(i,end='')
```

    01234


```python
#start with 5 and upto 10
for i in range(5,10):
    print(i,end=' ')
```

    5 6 7 8 9 


```python
print(type(x))
```

    <class 'list'>
    


```python
#using step of 3
for i in range(10,25,3):
    print(i,end=' ')

```

    10 13 16 19 22 


```python
for i in range(-5,10,2):
    print(i,end=' ')

```

    -5 -3 -1 1 3 5 7 9 

2. List[]:


```python
even=[2,4,6]
print(type(even))
```

    <class 'list'>
    


```python
fruits=['apple','guava','grapes']
type(fruits)
```




    list




```python
#to know the no. of elements in a list
```


```python
len(x)
```




    5




```python
print(len(x))
```

    5
    


```python
for i in fruits:
    print(i,end' ')
```


      File "<ipython-input-17-086990d0341b>", line 2
        print(i,end' ')
                     ^
    SyntaxError: invalid syntax
    



```python
even=list[2,4,6,8,10,12,14,16]
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-18-38d85b54ef3a> in <module>
    ----> 1 even=list[2,4,6,8,10,12,14,16]
    

    TypeError: 'type' object is not subscriptable



```python
even=[2,4,6,8,10,12,14,16]
```


```python
sum=0
for i in even:
    sum+=i
    print('sum=',sum)
```

    sum= 2
    sum= 6
    sum= 12
    sum= 20
    sum= 30
    sum= 42
    sum= 56
    sum= 72
    


```python
sum=0
for i in even:
    sum+=i
print('sum=',sum)
```

    sum= 72
    


```python
#library fn for sum for lists:
sum(even)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-22-af47c7c844b8> in <module>
          1 #library fn for sum for lists:
    ----> 2 sum(even)
    

    TypeError: 'int' object is not callable



```python
a=sum(even)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-23-fab8e11dd37b> in <module>
    ----> 1 a=sum(even)
    

    TypeError: 'int' object is not callable



```python
sum(even,start)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-24-daf4828d8aa2> in <module>
    ----> 1 sum(even,start)
    

    NameError: name 'start' is not defined



```python
sum(even,2)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-25-029f3833676a> in <module>
    ----> 1 sum(even,2)
    

    TypeError: 'int' object is not callable



```python
#test for prime no. from user i/p
n=int(input('number'))
for i in range(2,n//2+1):
    if n%2==0:
        flag==1
        print('not a prime no.')
        break
    else:
        print('Is a prime no.')
```

    number29
    Is a prime no.
    Is a prime no.
    Is a prime no.
    Is a prime no.
    Is a prime no.
    Is a prime no.
    Is a prime no.
    Is a prime no.
    Is a prime no.
    Is a prime no.
    Is a prime no.
    Is a prime no.
    Is a prime no.
    


```python
n=int(input('number'))
for i in range(2,n//2+1):
    if n%2==0:
        flag==1
        print('not a prime no.')
        break
else:                       #for else can also be used
    print('Is a prime no.')
```

    number29
    Is a prime no.
    


```python
for n in range(2,50):
    for i in range(2,n//2+1):
        if n%2==0:
            print(n,' not prime')
            break
    else:
        print(n," prime")
```

    2  prime
    3  prime
    4  not prime
    5  prime
    6  not prime
    7  prime
    8  not prime
    9  prime
    10  not prime
    11  prime
    12  not prime
    13  prime
    14  not prime
    15  prime
    16  not prime
    17  prime
    18  not prime
    19  prime
    20  not prime
    21  prime
    22  not prime
    23  prime
    24  not prime
    25  prime
    26  not prime
    27  prime
    28  not prime
    29  prime
    30  not prime
    31  prime
    32  not prime
    33  prime
    34  not prime
    35  prime
    36  not prime
    37  prime
    38  not prime
    39  prime
    40  not prime
    41  prime
    42  not prime
    43  prime
    44  not prime
    45  prime
    46  not prime
    47  prime
    48  not prime
    49  prime
    


```python
for n in range(2,50):
    for i in range(2,n//2+1):
        if n%i==0:
            break
    else:
        print(n," prime")
```

    2  prime
    3  prime
    5  prime
    7  prime
    11  prime
    13  prime
    17  prime
    19  prime
    23  prime
    29  prime
    31  prime
    37  prime
    41  prime
    43  prime
    47  prime
    


```python
#prog to print amtrix of alphabets
size=int(input("size of the sqr"))
for i in range(size):
    for j in range(size):
        print('A',end=' ')
    print()
    
```

    size of the sqr5
    A A A A A 
    A A A A A 
    A A A A A 
    A A A A A 
    A A A A A 
    


```python
size=int(input("size of the sqr"))
for i in range(size):
    for j in range(size):
        print('*',end=' ')
    print()
```

    size of the sqr7
    * * * * * * * 
    * * * * * * * 
    * * * * * * * 
    * * * * * * * 
    * * * * * * * 
    * * * * * * * 
    * * * * * * * 
    

##Indexing & slicing in lists:


```python
print(fruits)
```

    ['apple', 'guava', 'grapes']
    


```python
print(fruits[::-1])
```

    ['grapes', 'guava', 'apple']
    


```python
fruits+=['kiwi','melon']
```


```python
print(fruits)
```

    ['apple', 'guava', 'grapes', 'kiwi', 'melon']
    


```python
print(fruits[::-1])
```

    ['melon', 'kiwi', 'grapes', 'guava', 'apple']
    


```python
print(fruits*2)
```

    ['apple', 'guava', 'grapes', 'kiwi', 'melon', 'apple', 'guava', 'grapes', 'kiwi', 'melon']
    


```python
print(even)
```

    [2, 4, 6, 8, 10, 12, 14, 16]
    


```python
even=[100]
```


```python
print(even)
```

    [100]
    


```python
even=[2,4,6,8,10,12,14,16,100]
```


```python
#append an element in a list
even.append(200)
```


```python
print(even)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 100, 200]
    


```python
#insert at specified index:
even.insert(8,18)
```


```python
print(even)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18, 100, 200]
    


```python
#index fn 
even.index(18)
```




    8




```python
even.index(100,5)
```




    9




```python
#remove element
even.remove(100)
```


```python
print(even)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18, 200]
    


```python
even+=[20,24,8,12,16]
```


```python
print(even)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18, 200, 20, 24, 8, 12, 16]
    


```python
#get the frequency of element
even.count(8)
```




    2




```python
even.remove(:2)
```


      File "<ipython-input-57-7dc55bb630c1>", line 1
        even.remove(:2)
                    ^
    SyntaxError: invalid syntax
    



```python
#remove element at particular index
even.pop(10)
```




    20




```python
del even[2:4]
```


```python
print(even)
```

    [2, 4, 10, 12, 14, 16, 18, 200, 24, 8, 12, 16]
    


```python
l=len(even)
for i in range(0,n):
    print(even[i],"\t")
```

    2 	
    4 	
    10 	
    12 	
    14 	
    16 	
    18 	
    200 	
    24 	
    8 	
    12 	
    16 	
    


    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    <ipython-input-61-c1b07bedd997> in <module>
          1 l=len(even)
          2 for i in range(0,n):
    ----> 3     print(even[i],"\t")
    

    IndexError: list index out of range



```python
#add elements to a list from user
l=[]
n=int(input('enter the no. of elements'))
for i in range(0,n):
    ele=int(input('enter the element'))
    l.append(ele)
print(l)
```

    enter the no. of elements4
    enter the element10
    enter the element20
    enter the element30
    enter the element40
    [10, 20, 30, 40]
    


```python
mix=[24,'hello',True,2+3j]
```


```python
#continue command
for i in mix:
    if type(i)==str:
        continue
    print(i)
```

    24
    True
    (2+3j)
    


```python
for i in mix:
    if isinstance(i,str):
        continue
    print(i)
```

    24
    True
    (2+3j)
    


```python
print('hello')
```

    hello
    


```python

```
