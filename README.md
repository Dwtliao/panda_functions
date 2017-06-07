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
        
def extract_time(regpattern, timestr):
    import re
    if re.search(regex, timestr):
    
        timefound = re.search(regex, timestr)
        print 'time found: %s' % (timefound.group(0))
        timefoundstr = timefound.group(0)
    
    return timefoundstr
    
regex = r"[0-9][0-9]:[0-9][0-9]:[0-9][0-9]"

timefound = extract_time(regex, str( ['time string 13:07:06'] ))
timefound

time found: 13:07:06
Out[281]: '13:07:06'
```
