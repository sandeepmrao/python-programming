# functions on lists


```python
x=[2,5,6,48,-4,89]
```


```python
print(sum(x))
```

    146
    


```python
print(min(x))
```

    -4
    


```python
print(max(x))
```

    89
    


```python
x.sort() #sorting is done in ascending order
print(x)
```

    [-4, 2, 5, 6, 48, 89]
    


```python
x.reverse()
```


```python
print(x)
```

    [89, 48, 6, 5, 2, -4]
    


```python
y=[56,89,45,12,25,3,-9]
y.sort(reverse=True) #sort in descending order
print(y)
```

    [89, 56, 45, 25, 12, 3, -9]
    


```python
#append multuple values in lists:
y.extend([78,52,12])
print(y)
```

    [89, 56, 45, 25, 12, 3, -9, 78, 52, 12]
    


```python
#copy list:
z=y.copy() #shallow copy
print(z)
```

    [89, 56, 45, 25, 12, 3, -9, 78, 52, 12]
    

nested lists


```python
y[6]=[1,2,3]
```


```python
print(y)
```

    [89, 56, 45, 25, 12, 3, [1, 2, 3], 78, 52, 12]
    


```python
y[6][2]
```




    3




```python
mat=[[1,2,3],[4,5,6],[7,8,9]]
```


```python
for i in mat:
    print(i)
```

    [1, 2, 3]
    [4, 5, 6]
    [7, 8, 9]
    


```python
#sum of each row of matrix
for i in mat:
    print('sum of row',i,'= ',sum(i))
```

    sum of row [1, 2, 3] =  6
    sum of row [4, 5, 6] =  15
    sum of row [7, 8, 9] =  24
    


```python
#multiplication of value in list
even=list(range(0,20,2))
print(even)
#syntax for map: map(function,list/sequence)-returns map object
dble_even=map(lambda i:i*2,even)
print(dble_even)
```

    [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
    <map object at 0x000000A1E0480708>
    


```python
print(even)
dble_even=list(map(lambda i:i*2,even)) ## convert the map values into list
print(dble_even)
```

    [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
    [0, 4, 8, 12, 16, 20, 24, 28, 32, 36]
    


```python
#functions:
def double(x):
    return x*2
```


```python
double(10)
```




    20




```python
#calling our function-double
print(even)
dble_even=list(map(double,even)) ## convert the map values into list
print(dble_even)
```

    [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
    [0, 4, 8, 12, 16, 20, 24, 28, 32, 36]
    


```python
#filter function:
print(even)
sqr_even=list(filter(lambda i:i>10,even)) 
print(sqr_even)
```

    [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
    [12, 14, 16, 18]
    


```python
lst=list(range(50,101))
print(lst)
```

    [50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100]
    


```python
xmultple=list(filter(lambda i:i%5==0,range(50,101)))
print(xmultple)
```

    [50, 55, 60, 65, 70, 75, 80, 85, 90, 95, 100]
    


```python
def multiple(i):
    if i%5==0:
        return i
    else:
        exit()
```


```python
multple=list(filter(multiple,lst))
print(multple)
```

    [50, 55, 60, 65, 70, 75, 80, 85, 90, 95, 100]
    

## stack: list of values- insert & delete only from last: LILO


```python
st=[2,5,9,7,12]
#push/insert elemnt into stack
st.append(25)
```


```python
#delete last element from stack
ele=st.pop()
print(ele)
print(st)
```

    25
    [2, 5, 9, 7, 12]
    

## Queue can also be implemented: insert as last and del first


```python
#insert:
q=[5,9,3,7,8]
q.append(20)
print(q)
```

    [5, 9, 3, 7, 8, 20]
    


```python
#delete
#delays the procedure as all elements have to be moved
q.pop(0)
print(q)
```

    [9, 3, 7, 8, 20]
    

### using deque: efficient way of using queues


```python
from collections import deque
q1=deque([2,4,6,8])
q1.append(10)
print(q1)
```

    deque([2, 4, 6, 8, 10])
    


```python
ele=q1.popleft()
print(ele)
print(q1)
```

    2
    deque([4, 6, 8, 10])
    

## list comprehensions


```python
#loop var exists even after coming out of loop:
for i in range(5):
    print(i,'\t')
print(i)
```

    0 	
    1 	
    2 	
    3 	
    4 	
    4
    


```python
lst2=[j*2 for j in range(5)] #in this way, j is defined only for this loop
print(lst2)
print(j)
```

    [0, 2, 4, 6, 8]
    


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-12-e0b6fb7e6cff> in <module>
          1 lst2=[j*2 for j in range(5)]
          2 print(lst2)
    ----> 3 print(j)
    

    NameError: name 'j' is not defined



```python
##eg2:
mult_8=[k for k in range(50,101) if k%8==0]
print(mult_8)
```

    [56, 64, 72, 80, 88, 96]
    


```python
p=[(a,b) for a in [1,2,3] for b in [4,5,6]]
print(p)
```

    [(1, 4), (1, 5), (1, 6), (2, 4), (2, 5), (2, 6), (3, 4), (3, 5), (3, 6)]
    


```python
# display elements of list above average
lst=[range(5,30,2)]
avg=sum(lst)/len(lst)
print(lst)
print(avg)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-16-ece1ce0fbc3b> in <module>
          1 # display elements of list above average
          2 lst=[range(5,30,2)]
    ----> 3 avg=sum(lst)/len(lst)
          4 print(lst)
          5 print(avg)
    

    TypeError: unsupported operand type(s) for +: 'int' and 'range'


## strings: a sequence of char in single or double quotes


```python
s='hello world'
print(s)
```

    hello world
    


```python
print(s[3])
```

    l
    

### strings are immutable


```python
s[3]='L'
print(s)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-19-89666d1a8e81> in <module>
    ----> 1 s[3]='L'
          2 print(s)
    

    TypeError: 'str' object does not support item assignment



```python
print(s.upper())
print(s)
```

    HELLO WORLD
    hello world
    


```python
s.isdigit()
```




    False




```python
s.append('all')
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-22-306dca61fe6c> in <module>
    ----> 1 s.append('all')
    

    AttributeError: 'str' object has no attribute 'append'



```python
s1=list(s)
```


```python
print(s1)
```

    ['h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd']
    


```python
f,g=10,20
t='value of x= {} value of y {}'.format(f,g)
```


```python
print(t)
```

    value of x= 10 value of y 20
    


```python
print(f"value of x={10}")
```

    value of x=10
    


```python
print('hello')
```

    hello
    


```python

```
