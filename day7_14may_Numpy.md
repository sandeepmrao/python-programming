## Numpy is a package for arrays- numerical python


```python
import numpy as np #shortcut name to numpy
```


```python
np.__version__
```




    '1.18.1'



### create arrays


```python
#creating arrays from lists: ndarray class
x=[10,20,50,40,60,89]
a=np.array(x)
print(type(a))
print(a)
```

    <class 'numpy.ndarray'>
    [10 20 50 40 60 89]
    


```python
#creating arrays from tuples:
t=8,9,5,2
ta=np.array(t)
print(type(ta))
print(ta)
```

    <class 'numpy.ndarray'>
    [8 9 5 2]
    


```python
#create aray from range:
a=np.arange(2,20,3)
print(type(a))
print(a)
```

    <class 'numpy.ndarray'>
    [ 2  5  8 11 14 17]
    


```python
a=np.arange(2,20,3,dtype='float')
print(type(a))
print(a)
```

    <class 'numpy.ndarray'>
    [ 2.  5.  8. 11. 14. 17.]
    


```python
#creating array whr values are linearly spaced
x=np.linspace(10,15,20)#start,stop & no. of values to generate
print(type(x))  #the interval is calculated bythe sys depending on the no. of values
print(x)
```

    <class 'numpy.ndarray'>
    [10.         10.26315789 10.52631579 10.78947368 11.05263158 11.31578947
     11.57894737 11.84210526 12.10526316 12.36842105 12.63157895 12.89473684
     13.15789474 13.42105263 13.68421053 13.94736842 14.21052632 14.47368421
     14.73684211 15.        ]
    


```python
x=np.linspace(10,15,20,endpoint=False)#start,stop & no. of values to generate
print(type(x))  #the interval is calculated bythe sys depending on the no. of values
print(x)
```

    <class 'numpy.ndarray'>
    [10.   10.25 10.5  10.75 11.   11.25 11.5  11.75 12.   12.25 12.5  12.75
     13.   13.25 13.5  13.75 14.   14.25 14.5  14.75]
    


```python
x=np.linspace(10,15,20,endpoint=False, retstep=True)#start,stop & no. of values to generate
print(type(x))  #the interval is calculated bythe sys depending on the no. of values
print(x)
```

    <class 'tuple'>
    (array([10.  , 10.25, 10.5 , 10.75, 11.  , 11.25, 11.5 , 11.75, 12.  ,
           12.25, 12.5 , 12.75, 13.  , 13.25, 13.5 , 13.75, 14.  , 14.25,
           14.5 , 14.75]), 0.25)
    


```python
#log spacing:(default base is 10)
y=np.logspace(1,5)
print(type(y))
print(y)
```

    <class 'numpy.ndarray'>
    [1.00000000e+01 1.20679264e+01 1.45634848e+01 1.75751062e+01
     2.12095089e+01 2.55954792e+01 3.08884360e+01 3.72759372e+01
     4.49843267e+01 5.42867544e+01 6.55128557e+01 7.90604321e+01
     9.54095476e+01 1.15139540e+02 1.38949549e+02 1.67683294e+02
     2.02358965e+02 2.44205309e+02 2.94705170e+02 3.55648031e+02
     4.29193426e+02 5.17947468e+02 6.25055193e+02 7.54312006e+02
     9.10298178e+02 1.09854114e+03 1.32571137e+03 1.59985872e+03
     1.93069773e+03 2.32995181e+03 2.81176870e+03 3.39322177e+03
     4.09491506e+03 4.94171336e+03 5.96362332e+03 7.19685673e+03
     8.68511374e+03 1.04811313e+04 1.26485522e+04 1.52641797e+04
     1.84206997e+04 2.22299648e+04 2.68269580e+04 3.23745754e+04
     3.90693994e+04 4.71486636e+04 5.68986603e+04 6.86648845e+04
     8.28642773e+04 1.00000000e+05]
    


```python
y=np.logspace(1,5,num=5,dtype='int')
print(type(y))
print(y)
```

    <class 'numpy.ndarray'>
    [    10    100   1000  10000 100000]
    


```python
#2d array:
q=[[1,2,3],[4,5,6]]
a=np.array(q)
print(a)
```

    [[1 2 3]
     [4 5 6]]
    


```python
#3d array:
q1=[[[1,2,3],[4,5,6]],[[7,8,9],[10,11,12]]]
a1=np.array(q1)
print(a1)
```

    [[[ 1  2  3]
      [ 4  5  6]]
    
     [[ 7  8  9]
      [10 11 12]]]
    


```python
#0d arrays: single value
s=np.array(89)
print(type(s),'\n',s)
```

    <class 'numpy.ndarray'> 
     89
    


```python
#create array of 2x3 of ones 
x=np.ones((2,3),dtype='int')
print(x)
```

    [[1 1 1]
     [1 1 1]]
    


```python
x=np.ones((5),dtype='int')
print(x)
```

    [1 1 1 1 1]
    


```python
w=np.full((3,4),'h')
print(w)
```

    [['h' 'h' 'h' 'h']
     ['h' 'h' 'h' 'h']
     ['h' 'h' 'h' 'h']]
    


```python
f=np.zeros((3,3))
print(f)
```

    [[0. 0. 0.]
     [0. 0. 0.]
     [0. 0. 0.]]
    

## access elements in arrays
indexing and slicing:
index of an array starts from 0


```python
e=np.linspace(10,15,20,)
e=np.array(e)
print(type(e))  
print(e)
```

    <class 'numpy.ndarray'>
    [10.         10.26315789 10.52631579 10.78947368 11.05263158 11.31578947
     11.57894737 11.84210526 12.10526316 12.36842105 12.63157895 12.89473684
     13.15789474 13.42105263 13.68421053 13.94736842 14.21052632 14.47368421
     14.73684211 15.        ]
    


```python
print(e[-1])
```

    15.0
    


```python
print(e[0])
```

    10.0
    


```python
#slicing:
print(e[5:])
```

    [11.31578947 11.57894737 11.84210526 12.10526316 12.36842105 12.63157895
     12.89473684 13.15789474 13.42105263 13.68421053 13.94736842 14.21052632
     14.47368421 14.73684211 15.        ]
    


```python
print(e[::-1])
```

    [15.         14.73684211 14.47368421 14.21052632 13.94736842 13.68421053
     13.42105263 13.15789474 12.89473684 12.63157895 12.36842105 12.10526316
     11.84210526 11.57894737 11.31578947 11.05263158 10.78947368 10.52631579
     10.26315789 10.        ]
    


```python
r=[[1,2,3],[4,5,6],[7,8,9]]
z=np.array(r)
print(z)
```

    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    


```python
print(z[1][2]) 
```

    6
    


```python
g=[[[1,2,3],[4,5,6]],[[7,8,9],[10,11,12]]]
g=np.array(g)
print(g)
```

    [[[ 1  2  3]
      [ 4  5  6]]
    
     [[ 7  8  9]
      [10 11 12]]]
    


```python
print(g[1][0][2])
```

    9
    


```python
print(g[0][0][2])
```

    3
    


```python
p=np.array([1,4,8,9])
q=p.copy()
print(p,'\t',q)
```

    [1 4 8 9] 	 [1 4 8 9]
    


```python
p[3]=12
print(p,'\t',q) #shallow copy:changes made are not reflected in q
r=p.view() # changes made in p can be seen in r
p[2]=10
print(p,'\t',r)
```

    [ 1  4  8 12] 	 [1 4 8 9]
    [ 1  4 10 12] 	 [ 1  4 10 12]
    


```python
type(q)
```




    numpy.ndarray




```python
type(r)
```




    numpy.ndarray




```python
print(q.base) #for copy, base is none
print(r.base) # for view(), base is array
```

    None
    [ 1  4 10 12]
    


```python
print(p.size)
```

    4
    


```python
print(p.shape)
```

    (4,)
    


```python
r1=[[1,2,3],[4,5,6],[7,8,9]]
r1=np.array(r1)
print('no. of elements in array is: ',r1.size,'\n','row x col of array is: ',r1.shape)

```

    no. of elements in array is:  9 
     row x col of array is:  (3, 3)
    


```python
print(r1.dtype)
r2=r1.astype('float32')
print(r2.dtype)
```

    int32
    float32
    


```python
#reshaping the array into other dimensions:
p1=p.reshape(2,2) # from 1-d to 2-d
p2=p.reshape(2,2,-1) # from 1-d to 3-d
```


```python
print(p1,'\n','\n',p2)
```

    [[ 1  4]
     [10 12]] 
     
     [[[ 1]
      [ 4]]
    
     [[10]
      [12]]]
    

### operations on arrays: vectorization


```python
a1=np.array([1,2,3,4,5,6])
a2=np.array([5,6,7,8,9,10])
print(a1+a2)  #to add corresponding elements in array
```

    [ 6  8 10 12 14 16]
    


```python
a3=a1+a2
print(type(a3),'\n',a3)
```

    <class 'numpy.ndarray'> 
     [ 6  8 10 12 14 16]
    


```python
print(a1,'\n',a1>4)
```

    [1 2 3 4 5 6] 
     [False False False False  True  True]
    


```python
#element wise adition
x1=np.ones((3,3))
x2=np.full((3,3),8)
print(x1+x2)
```

    [[9. 9. 9.]
     [9. 9. 9.]
     [9. 9. 9.]]
    


```python
#element wise multiplication: (*)
x1=np.ones((3,3))
x2=np.full((3,3),8)
print(x1*x2)
```

    [[8. 8. 8.]
     [8. 8. 8.]
     [8. 8. 8.]]
    


```python
#matrix multiplication- (.dot())
x1.dot(x2)
```




    array([[24., 24., 24.],
           [24., 24., 24.],
           [24., 24., 24.]])




```python
print(a1)
print('sum of elements: ',a1.sum())
print('min of elements: ',a1.min())
print('max of elements: ',a1.max())
print('mean of elements: ',a1.mean())
print('cumilative sum of elements: ',a1.cumsum())
print('std deviatn of elements: ',a1.std())
print('variance of elements: ',a1.var())
```

    [1 2 3 4 5 6]
    sum of elements:  21
    min of elements:  1
    max of elements:  6
    mean of elements:  3.5
    cumilative sum of elements:  [ 1  3  6 10 15 21]
    std deviatn of elements:  1.707825127659933
    variance of elements:  2.9166666666666665
    

#### numpy math operation


```python
np.sqrt(a1) 
```




    array([1.        , 1.41421356, 1.73205081, 2.        , 2.23606798,
           2.44948974])




```python
np.cbrt(a1) # cube rrot of elements
```




    array([1.        , 1.25992105, 1.44224957, 1.58740105, 1.70997595,
           1.81712059])




```python
np.abs(a1)
```




    array([1, 2, 3, 4, 5, 6])




```python
np.product(a1) #product of elemnts
```




    720




```python
print(np.log(a1)) # by default base is e
print(np.log2(a1))
print(np.log10(a1))
```

    [0.         0.69314718 1.09861229 1.38629436 1.60943791 1.79175947]
    [0.         1.         1.5849625  2.         2.32192809 2.5849625 ]
    [0.         0.30103    0.47712125 0.60205999 0.69897    0.77815125]
    

#### looping thru array elements:


```python
for i in a1:
    print(a1)
```

    [1 2 3 4 5 6]
    [1 2 3 4 5 6]
    [1 2 3 4 5 6]
    [1 2 3 4 5 6]
    [1 2 3 4 5 6]
    [1 2 3 4 5 6]
    


```python
for i in a1:
    print(i)
```

    1
    2
    3
    4
    5
    6
    


```python
for i in r1:
    print(i)
```

    [1 2 3]
    [4 5 6]
    [7 8 9]
    


```python
for row in r1:        # looping for 2d array
    for i in row:
        print(i,end=" ")
    print()
```

    1 2 3 
    4 5 6 
    7 8 9 
    


```python
for id,ele in np.ndenumerate(r1):   #ennumerate elements in anarray
    print(id,ele)
```

    (0, 0) 1
    (0, 1) 2
    (0, 2) 3
    (1, 0) 4
    (1, 1) 5
    (1, 2) 6
    (2, 0) 7
    (2, 1) 8
    (2, 2) 9
    


```python
a4=np.concatenate((a1,a2))
print(a4)
```

    [ 1  2  3  4  5  6  5  6  7  8  9 10]
    


```python
#sorting in array:
s1=[5,23,41,89,65,-16,-3]
np.sort(s1)
```




    array([-16,  -3,   5,  23,  41,  65,  89])



#### generate random nos. b/w 0 to 1 


```python
v=np.random.rand()
print(v)
```

    0.4305085597722683
    


```python
v1=np.random.rand(2,3)
print(v1)
```

    [[0.6008191  0.09279811 0.21447973]
     [0.2810344  0.38605211 0.46648897]]
    


```python
# save the array into a file in the root directory:
np.savetxt('randmfle.txt',v1)
```


```python
# getting file contents into array(.txt file)
p2=np.loadtxt('randmfle.txt')
```


```python
print(p2)
```

    [[0.6008191  0.09279811 0.21447973]
     [0.2810344  0.38605211 0.46648897]]
    

#### quiz questns:


```python
def func(x,y):
    return x+y
```


```python
z=func(3,func(4,5))
print(z)
```

    12
    


```python
def prt(f,s):
    n=f+' '+s
    return n
```


```python
f=input('f')
s=input('s')
n=prt(f,s)
print(n)
```

    fanand
    sdhs
    anand dhs
    


```python

```
