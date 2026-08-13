We can chain and combine NumPy operations to ask more complicated questions about the data in an array. For example, we can check whether all elements of an array are less than a particular value, as in the function below:

```py-cell
import numpy as np

def check_all_less_than_threshold(arr, threshold):
    return (arr < threshold).all()

a = np.array([1, 2, 3])

print(check_all_less_than_threshold(a, 10))
print(check_all_less_than_threshold(a, 2))
```

Within the function, the order of operations applies as normal so `arr < threshold` is evaluated first, returning a boolean array. The entries of this array describe whether the corresponding entries of `arr` are less than the threshold. The `.all()` method is then called on this boolean array, returning a single boolean value that describes whether all entries of the array are `True`.

Combining operations like this can be a compact and computationally efficient way to ask questions about the data in an array.