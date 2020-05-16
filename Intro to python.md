```python
x=11
print(x)
```

    11
    


```python
type(x)
```




    int




```python
y=230.5689
print(y)
```

    230.5689
    


```python
print(type(y))
```

    <class 'float'>
    


```python
print(type(y),y)
```

    <class 'float'> 230.5689
    


```python
print('hello world')
```

    hello world
    


```python
s='hello world'
```


```python
print(type(s),s)
```

    <class 'str'> hello world
    


```python
b1=True
b2=False
print('b1=',b1)
print('b2=',b2)
```

    b1= True
    b2= False
    


```python
print(type(b1),b1) #boolean data type
```

    <class 'bool'> True
    


```python
c1=5+5j
c2=10+2.5j
print(type(c2))
type(c1)  #complex no. data type
```

    <class 'complex'>
    




    complex



#Assignments:


```python
###multiple assigments:
x,y,z=100,10.9,True
```


```python
print(type(x),x)
print(type(y),y)
print(type(z),z)
```

    <class 'int'> 100
    <class 'float'> 10.9
    <class 'bool'> True
    

###dynamic typing


```python
x=100
print(type(x),x)
x='hello'
print(type(x),x)
```

    <class 'int'> 100
    <class 'str'> hello
    

##Arithmatic operators


```python
a,b=10,3
print(a/b)
print(a//b)
```

    3.3333333333333335
    3
    


```python
## // is integer division
## / is real no. division
```


```python
a,b,c=90,10.55,'hello'
print(a+b)
```

    100.55
    


```python
print(c)
```

    hello
    


```python
print(a+c)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-23-29620a3af8d7> in <module>
    ----> 1 print(a+c)
    

    TypeError: unsupported operand type(s) for +: 'int' and 'str'



```python
d=' world'
print(c+d)
```

    hello world
    


```python
# + works as concatenation for the same data type
```


```python
x=100
x+=10  # compound assignment
```


```python
print(a)
```

    90
    


```python
print(x)
```

    110
    


```python
i=5
i*=2**3
print(i)
```

    40
    


```python
print('enter the no.')
input(n)
```

    enter the no.
    


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-31-b3313253f269> in <module>
          1 print('enter the no.')
    ----> 2 input(n)
    

    NameError: name 'n' is not defined



```python
f(n>90)
print('suporo')
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-32-d9a6f870b632> in <module>
    ----> 1 f(n>90)
          2 print('suporo')
    

    NameError: name 'f' is not defined


a=10+5j
b=int(a)
print(a)


```python
a=10
print(complex(a))
```

    (10+0j)
    

##Input & assignemnts


```python
x=input("enter")
print(type(x),x)
```

    enter10
    <class 'str'> 10
    


```python
x=int(x)
print(type(x),x)
```

    <class 'int'> 10
    

if statement syntax


```python
if x>0:
    print(x)
    print("+ve")
else:
    print('-ve')
```

    10
    +ve
    


```python
#code to find largest of 2 nos from user input:
```


```python
x=input('enter the 1st no.')
y=input('enter the 2nd no.')
if x>y:
    print('the largest is: ',x)
else:
    print('the largest is: ',y)
```

    enter the 1st no.10
    enter the 2nd no.25
    the largest is:  25
    


```python
max(10,20,30)
```




    30




```python
max(10,60,20,45,56)
```




    60




```python
print(max(10,30,20),'is bigger')
```

    30 is bigger
    


```python
x=(max(10,35,56))
```


```python
# shortcut to single if-else statement:(not valid for single if statements)
print('positive') if x>0 else print('not +ve')
```

    positive
    


```python
x*=-1
print('positive') if x>0 else print('not +ve')
```

    not +ve
    

##input a point(x,y) and radius and check if the point lies inside the circle


```python
x=input('enter the x coordinate')
y=input('enter the y coordinate')
r=input('enter the radius of circle')
import math
math.sqrt(d)
d=sqrt(x**2+y**2)
print('inside the circle') if d<=r else print('outside circle')
```

    enter the x coordinate10
    enter the y coordinate20
    enter the radius of circle5
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-47-7db4026d0f0c> in <module>
          3 r=input('enter the radius of circle')
          4 import math
    ----> 5 math.sqrt(d)
          6 d=sqrt(x**2+y**2)
          7 print('inside the circle') if d<=r else print('outside circle')
    

    TypeError: must be real number, not str



```python
a=sqrt(16)
print(a)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-48-94cc58d6f1c7> in <module>
    ----> 1 a=sqrt(16)
          2 print(a)
    

    NameError: name 'sqrt' is not defined



```python
import math
math.sqrt(a)
a=sqrt(16)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-49-55308e031c50> in <module>
          1 import math
          2 math.sqrt(a)
    ----> 3 a=sqrt(16)
    

    NameError: name 'sqrt' is not defined



```python
import math
x=int(input('enter the x coordinate'))
y=int(input('enter the y coordinate'))
r=int(input('enter the radius of circle'))
d=math.sqrt(x**2+y**2)
 if d<=r:
        print('inside the circle')
else:
        print('outside circle')
```


      File "<ipython-input-55-76455faf04d9>", line 6
        if d<=r:
        ^
    IndentationError: unexpected indent
    



```python
import math
x=int(input('enter the x coordinate'))
y=int(input('enter the y coordinate'))
r=int(input('enter the radius of circle'))
d=math.sqrt(x**2+y**2)
if d<=r:
    print('inside the circle')
else:
    print('outside circle')
```

    enter the x coordinate10
    enter the y coordinate20
    enter the radius of circle5
    outside circle
    

#loops: 1.while


```python
#while syntax(note the indentation)
i=1
while i<=10:
    print(i)
    i+=1
print('got out of loop')
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    got out of loop
    


```python
i=1
while i<=10:
    print(i,end=' ')
    i+=1
print('got out of loop')
```

    1 2 3 4 5 6 7 8 9 10 got out of loop
    


```python
##prob 1: display proper divisors of n
n=int(input('enter no.'))
i=2
while i<=(n//2):
    if n%i==0:
        print(i,end=' ')
    i+=1
```

    enter no.18
    2 3 6 9 


```python
# check if n is prime
n=int(input('enter the no.'))
i=2
flag=1
while i<=n//2:
    if n%i==0:
        flag=0
        break
    i+=1
if flag==1:
    print(n,' Is a prime no.')
else:
    print(n,'Not a prime no.')
```

    enter the no.71
    71  Is a prime no.
    


```python

```
