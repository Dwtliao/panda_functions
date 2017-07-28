# py_panda_functions
handy py panda functions developed/found over time

```
def remove_dups(df, col_to_remove):
    df.sort_values(by=[col_to_remove], inplace=True)
    df2 = df.groupby(col_to_remove).first().reset_index()
    return df2

def filter_feature_by_value(df, feature, value_gte):
    return df[(df[feature] >= int(value_gte))]
    
def sort_by_2features(df, feature1, feature2):
    df.sort_values(by=[feature1, feature2], inplace=True)
    return df    

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


def get_units_sql(dbcur, dbconn, df_list):

    sql = "SELECT un.id as unit_id \
        , un.name as unit_name \
        , un.department_id as dept_id \
        FROM units as un \
        where un.id in (%s) "

def intlist_tostring(int_list):
    stmp = ''

    for index, element in enumerate(int_list):
        if index != 0:
            stmp += ','

        stmp += '\"' + str(element) + '\"'

    return stmp
    
def get_sql(dbcur, dbconn, df_list, df_list_key, sql, table):

# df_list_keys are columns values to become string "integers" for sql
    int_ids = df_list[df_list_key].tolist()
    ids_string = intlist_tostring(int_ids)
    sql = sql % ids_string
    

```
