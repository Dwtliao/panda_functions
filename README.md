# py_panda_functions
handy py panda functions developed/found over time

```
def pd_fillnulls(df, column, fillvalue):
    
    df[column].fillna(fillvalue, inplace=True)
    
def pd_replacenulls(df, column, fillvalue):
    
    df[column].replace(np.nan, fillvalue, inplace=True) 
    
def pd_astype_int(df, column, datatype):
    
    if datatype == 'int':
        df[column] = df[column].astype(int)
        
```
