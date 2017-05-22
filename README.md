# numpy_functions
handy numpy functions developed/found over time

```
def delete_1st_arrayrow(arr):
    return np.delete(arr, np.s_[0:1], 0)   #delete row 0, axis=0

def delete_1st_arraycol(arr):
    return np.delete(arr, np.s_[0:1], 1)   #delete column 0, axis=1
    
def np_sum_row_columns(array_in):
    #add the column values of each row and return each row's sum
    return np.sum(array_in, axis=1)

def np_sum_each_column(array_in):
    #add the row values of each column and return 1 row of each column's total sum
    return np.sum(array_in, axis=0)
    
```
