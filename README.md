# CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric

The goal of this project is to ingest into Fabric DataMart, clean and transform the data, create model and visualize the end result

#Data Ingestion 

This project made use of DataMart in Microsoft fabric as our preferred mode of data ingestion because DataMart is efficient when connecting to different tables from different data sources. In our scenario, the two dataset we use are CSVs file located in onedrive folder.  

Connection were made to the 2 dataset using Get Data and use *Text/CSV* as API connector
![Getting the Data](https://github.com/Ainaganiu/CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric/blob/main/Pictures/ingestion.png)

#Data Transformation

After loading the dataset transformation steps such promoting headers, renaming rows, deleting unwanted columns, removing duplicates were performed as part of the transformation model for the two table

Table 1: CO2_2021
![Table 1](https://github.com/Ainaganiu/CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric/blob/main/Pictures/table1.png)

Table 2: Location
![Table 2](https://github.com/Ainaganiu/CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric/blob/main/Pictures/table2.png)
