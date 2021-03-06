# data_cleaning
data cleaning checklist &amp; relevant scripts in python3


![a general process from data cleaning with R](https://github.com/CS0000/data_cleaning/blob/main/process.png)               


This note will illustrate a more detailed checklist along with processing scripts, which will be demonstrated on an adjusted data based on Kaggle.

I don't suggest applying the process above mechanically. Because after the fixing and imputation, the normalizing result may have changed, which may introduces duplicated process.
However, the given process is highly referable for a real-world data cleaning.

## check list
### 1. import raw data into python        
**import `.csv`, `.tsv`, `.xlsx` using pandas**    
:zap: set index? header?          
> `header = None, index_col = None`    
> avoid setting the sampleID column to index, or assume the first row to be header at the data import stage, unless you are fully aware that there are no repeated row or column names in the given data. Setting index to duplicated **columns** may lead to troubles in pandas.


### 2. check duplicated samples/observations/rows & features/columns    
whether to remove the duplicated rows&columns, it depends. For completely identical rows&columns, it generally should be fine to remove them. However, for those columns/rows with duplicated column/row names but different values,
it would be treated more prudently. Communicating with the data collectors and decide which row/column to remove.     

All the processes, like deleting or modifying the value in the tables, should be recorded in scripts, and a data cleaning log file. (...and inform your supervisors too.)

The demonstrating jupyter notebook only elaborate the situation with two duplicated rows/columns.

Then it's supposed to get a dataframe with unique rows and columns names.

### 3. use pandas_profiling to get an overall view    
pandas_profiling is a very useful tool to demonstrate the distribution and general pattern of data.    
use pandas_profiling to figure out a general view of data, like the percentage of missing values, the proportion of different data types (categorical or numerical), etc.
It can be very helpful to check if the data type for each variable is correct, as well as giving a general overview of data, as long as the data types are reasonable.
For example, if the variable "age" presented to be a categorical data type, it would alarm you that maybe there are some string characters mixed in this column, and you will go to check.

### 4. fix data type
- data type: each column has a unique data type, numerical or categorical. After step 3 you may detect the inconsistency of data types through output.         
- It would be better to record the change process, both in scripts, and a readme file.   
- Although not mentioned in the demonstrated notebook, time variable also should be concerned if necessary.      
- In some dirty data set, the string characters may have leading or trailing blank, which may cause trouble to the downstream analysis.            


### 4. summarize missing data
### 5. reasonable data     
distribution     
outlier, maximum/minimum reasonable

### 6. arrange raw and processed data     
raw_data/  and  processed_data/, separated folders, scripts or processing codes connected them together

### 7. version control    
what about an unexpected update of raw data ?
