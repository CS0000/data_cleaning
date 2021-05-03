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
> avoid setting the sampleID column to index at the data import stage. Because you may not be aware of the existence of duplicated ID. Setting index to duplicated row may lead to troubles. 
   
