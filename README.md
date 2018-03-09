# csv
import pandas as pd 
from collections import defaultdict  
file_name = 'temp.csv' 
data = pd.read_csv('file_name') 
new_df = defaultdict(dict) 
for i in range(len(data)):    
this_data = data.iloc[i]    
name, dow = str(this_data['Category']), str(this_data['Sales per employee (y)'])    
value = int(this_data['Sales per employee (value)'])    
new_df[name][dow] = value 
new_df = pd.DataFrame(new_df) 
new_df.to_csv('file_name')
