## Optimal way of finding mean in python
Code optimization isn't needed to be done only by machines but also by us. Our coding habit and technique we choose have consequences either with space or time complexity. One simple mistake and yet often we do in daily coding life is with the python list. 

Python provides simplicity in writing code doesn't mean we can use any functions or library to achieve the goal. Consider a simple example, where you want to find mean of python list of integers. Below snippet of code explains various ways to achieve it. 

```
import time
import statistics
import numpy as np

def mean_normal(list_data):
    """
        Calculate mean of python list normaly
        input: list of int or float
        output: mean value
    """    
    start = time.time()
    avg = sum(list_data)/len(list_data)
    end = time.time()
    print("avg: {} & Time taken by mean_normal: {:.5f} sec".format(avg, end-start))
    return avg

def mean_statistics(list_data):
    """
        Calculate mean of python list using statistics lib
        input: list of int or float
        output: mean value
    """    
    start = time.time()
    avg = statistics.mean(list_data)
    end = time.time()
    print("avg: {} & Time taken by mean_statistics: {:.5f} sec".format(avg, end-start))
    return avg

def mean_numpy_with_list(list_data):
    """
        Calculate mean of python list using numpy lib
        input: list of int or float
        output: mean value
    """    
    start = time.time()
    avg = np.mean(list_data)
    end = time.time()
    print("avg: {} & Time taken by mean_numpy_with_list: {:.5f} sec".format(avg, end-start))
    return avg

def mean_numpy_with_array(array_data):
    """
        Calculate mean of numpy array using numpy lib
        input: 1-d numpy array
        output: mean value
    """    
    start = time.time()
    avg = np.mean(array_data)
    end = time.time()
    print("avg: {} & Time taken by mean_numpy_with_array: {:.5f} sec".format(avg, end-start))
    return avg
```

Now the selection of data type (float or int) also has an impact on each method. For example, results below are calculated using **integer list** of 3000000 lengths.  Clearly, mean_normal() method is the winner without NumPy library. On the other side, when using NumPy library, numpy array is extremely faster to calculate mean.  
```
# Test with int range
if __name__ == '__main__':
    data = list(range(3000000))
    mean_normal(data)
    mean_statistics(data)
    mean_numpy_with_list(data)
    mean_numpy_with_array(np.array(data))
```
*Output:*
```
avg: 1499999.5 & Time taken by mean_normal: 0.11733 sec
avg: 1499999.5 & Time taken by mean_statistics: 2.50410 sec
avg: 1499999.5 & Time taken by mean_numpy_with_list: 0.28698 sec
avg: 1499999.5 & Time taken by mean_numpy_with_array: 0.00589 sec
```
In case of **Float list** of same length, we have similar results where mean_normal() and mean_numpy() methods are the winner.
```
# Test with float range
if __name__ == '__main__':
    data = list(np.linspace(500,1000,3000000))
    mean_normal(data)
    mean_statistics(data)
    mean_numpy_with_list(data)
    mean_numpy_with_array(np.array(data))
```
*Output:*
```
avg: 749.9999999999993 & Time taken by mean_normal: 0.29277 sec
avg: 750.0 & Time taken by mean_statistics: 5.58369 sec
avg: 749.9999999999997 & Time taken by mean_numpy_with_list: 0.32793 sec
avg: 749.9999999999997 & Time taken by mean_numpy_with_array: 0.01073 sec
```

## Conclusion
NumPy library provide faster operation on numbers than the default methds. So use **NumPy library in combination of numpy array** whenever possible. If you want to find mean without any library, use **mean_normal()** method.
(NOTE: Do not use NumPy with list as can be seen, time complexity is more with list.)

