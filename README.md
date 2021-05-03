# data_cleaning
data cleaning checklist &amp; relevant scripts in python3

a general process from data cleaning with R.pdf
![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/80de7808-5c1d-4cbf-bee9-8794d6b5b7d0/Screenshot_2021-05-02_at_1.02.24_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/80de7808-5c1d-4cbf-bee9-8794d6b5b7d0/Screenshot_2021-05-02_at_1.02.24_AM.png)
This note will illustrate a more detailed checklist along with processing scripts, which will be demonstrated on an adjusted data based on Kaggle. 

I don't suggest applying the process above mechanically. Because after the fixing and imputation, the normalizing result may have changed, which may introduces duplicated process. 
However, the given process is highly referable for a real-world data cleaning. 

## check list 
1. Can the raw data be imported ?     
    import .csv, .tsv, .xlsx in python using pandas    
    :zap: set index? header?       
    avoid setting the sampleID column to index at the data import stage. Because you may not be aware of duplicated ID. Setting index to duplicated row may lead to troubles. 
   
