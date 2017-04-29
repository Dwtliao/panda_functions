# numpy_functions
handy numpy functions developed/found over time

```
def delete_1st_arrayrow(arr):
    return np.delete(arr, np.s_[0:1], 0)   #delete row 0, axis=0

def delete_1st_arraycol(arr):
    return np.delete(arr, np.s_[0:1], 1)   #delete column 0, axis=1
```
