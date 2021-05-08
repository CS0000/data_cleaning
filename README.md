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
whether to remove the duplicated rows&columns, it depends. For completely identical rows&columns, it should be ok to remove them. but for 
### 3. use pandas_profiling to get an overall view    
### 4. fix data type
data type: each column has a unique data type, numerical or categorical...      
fix data type if inconsistency detected       
record the change process, both in scripts, and a readme file    
time variable     
string characters: trim leading or tailing spaces


### 4. summarize missing data
### 5. reasonable data     
distribution     
outlier, maximum/minimum reasonable

### 6. arrange raw and processed data     
raw_data/  and  processed_data/, separated folders, scripts or processing codes connected them together

### 7. version control    
what about an unexpected update of raw data ?


