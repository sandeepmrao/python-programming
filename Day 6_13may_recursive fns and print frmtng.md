## Recursive fns: 
termination condtn should be provided in order to avouid falling into an infinite loop


```python
def factorial(n):
    if (n>0):
        if n==0:
            return 1
        else: 
            return n * factorial(n-1) # call to itself
    else:
        print('invalid input')
```


```python
factorial(5)
```

    invalid input
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-13-637175d621a4> in <module>
    ----> 1 factorial(5)
    

    <ipython-input-12-eea345c0ec53> in factorial(n)
          4             return 1
          5         else:
    ----> 6             return n * factorial(n-1) # call to itself
          7     else:
          8         print('invalid input')
    

    <ipython-input-12-eea345c0ec53> in factorial(n)
          4             return 1
          5         else:
    ----> 6             return n * factorial(n-1) # call to itself
          7     else:
          8         print('invalid input')
    

    <ipython-input-12-eea345c0ec53> in factorial(n)
          4             return 1
          5         else:
    ----> 6             return n * factorial(n-1) # call to itself
          7     else:
          8         print('invalid input')
    

    <ipython-input-12-eea345c0ec53> in factorial(n)
          4             return 1
          5         else:
    ----> 6             return n * factorial(n-1) # call to itself
          7     else:
          8         print('invalid input')
    

    <ipython-input-12-eea345c0ec53> in factorial(n)
          4             return 1
          5         else:
    ----> 6             return n * factorial(n-1) # call to itself
          7     else:
          8         print('invalid input')
    

    TypeError: unsupported operand type(s) for *: 'int' and 'NoneType'



```python
#display even nos. b/w n1 & n2:
def disp_even(ll,ul):
    if ll>ul:
        return
    elif ll%2==0:
        print(ll,end=' ')
    disp_even(ll+1,ul)
        
        
```


```python
disp_even(5,10)
```

    6 8 10 


```python
#display values b/w n1 & n2 using recursion:
def disp(n1,n2):
    if n1>n2:
        return
    else:
        print(n1,end=' ')
    disp(n1+1,n2)    
```


```python
disp(5,10)
```

    5 6 7 8 9 10 


```python
disp(10,4)
```


```python
disp(n2=10,n1=4)
```

    the nos are:  4 the nos are:  5 the nos are:  6 the nos are:  7 the nos are:  8 the nos are:  9 the nos are:  10 


```python
#sum of digits using recursion:
def sum_d(n):
    if n==0:
        return 0
    else:
        return n%10+sum_d(n//10)
```


```python
sum_d(115)
```




    7




```python
sum_d(0)
```




    0




```python
#list of digits of a no.
l=[]
def list_d(n):
    if n==0:
        return l[::-1]
    else:
        l.append(n%10)
        return list_d(n//10)
        
```


```python
list_d(54321)
```




    [5, 4, 3, 2, 1, 5, 4, 3, 2, 1, 1, 2, 3, 4, 5]




```python
print(x)
```

    [5, 4, 3, 2, 1, 1, 2, 3, 4, 5]
    


```python
list_d(561)
```




    []



### Random nos.: (useful for Machine learning)


```python
#random integers:
import random
r1=random.randrange(5,20) #random nos. from 0to 5
print(r1)
```

    17
    


```python
#random integers:
import random
r1=random.randrange(5,30,3) #random nos. from 0to 5
print(r1)
```

    17
    

### random elements from sequences:


```python
# choose one no. randomly in a given dat struc.
x=2,5,8,9,12
a=random.choice(x)
print(a)
```

    12
    


```python
# choose multiple no. randomly in a given dat struc.
x=2,5,8,9,12
a=random.choices(x,k=2)
print(a)
```

    [8, 12]
    


```python
# choose multiple no. randomly in a given dat struc.
x=2,5,8,9,12
a=random.choices(x,k=4)
print(a)
```

    [5, 12, 12, 5]
    


```python
print(type(x))
```

    <class 'tuple'>
    


```python
#seed fn 
random.seed(1)
random.choices(range(50,100),k=4)
```




    [56, 92, 88, 62]



## input/output:


```python
#to evaluate the input expression:
n=input('enter the value')
print(eval(n))
```

    enter the value10*2-5
    15
    


```python
#output: unformatted
x,y=100,10
print(x,y)
```

    100 10
    


```python
print(x,y,sep=';',end='$')
```

    100;10$

#### formatted output:


```python
#1.string format:
print('x={}  y={}'.format(x,y))
```

    x=100  y=10
    


```python
print('x={a}  y={b}'.format(b=x,a=y))
```

    x=10  y=100
    


```python
#2. string % values
#string contains specifiers: %f %f %e %E %g %G....
s,d=2.3654,8.9654
print('s=%f d=%f'%(s,d))
```

    s=2.365400 d=8.965400
    

#### %f for float, %d for integers, %s for string,%o for octal, %x for hexa decimal,


```python
#precision  .  limits the char to display:
q,w='hello tom',19.56478
print('q=%.5s' %(q))  #limits the print of no. of strings
print('w=%.2f'%(w))  #limits the nos. after the decimal point
```

    q=hello
    w=19.56
    


```python

```
