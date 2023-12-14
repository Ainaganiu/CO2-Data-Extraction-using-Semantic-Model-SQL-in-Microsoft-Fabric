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

#Data Modelling

The two tables were merge together using common keys in both common tables *PlantID* using Many-to_One as the relationship (Cardinality)

![model](https://github.com/Ainaganiu/CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric/blob/main/Pictures/model.png)

#Data Query

In this project we make use of two approach to query the dataset. We use the visualize quary capabilities in Semantic Model in of Microsoft Fabric to query the dataset. The folloing steps were performed.
1. Ingesting from the source data
2. Viewing the table
3. Choosing the desired columns
4. Filtering by columns
5. Group values using Aggregation

![visual Query 1](https://github.com/Ainaganiu/CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric/blob/main/Pictures/visualquery1.png)

Also the view query also has the ability to generate the sql codes for the steps we performed using drag and drop features of the visual query

![sql codes](https://github.com/Ainaganiu/CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric/blob/main/Pictures/sqlcodes.png)

**Ouput**
![visualQueryResult](https://github.com/Ainaganiu/CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric/blob/main/Pictures/visualqueryoutput.png)

## Query with SQL Codes

This SQL code in picture below is a query that retrieves aggregated information about carbon emissions and fuel consumption from two tables: [CO2_2021] and [US power plant locations]. The data is grouped by various columns, and aggregate functions are used to calculate total and average emissions, as well as total fuel consumption. Here's a breakdown of the code:

![SQL Codes](https://github.com/Ainaganiu/CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric/blob/main/Pictures/sqlqueriescodes.png)

**Output**

![query output](https://github.com/Ainaganiu/CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric/blob/main/Pictures/queryoutput.png)

![output visual 2](https://github.com/Ainaganiu/CO2-Data-Extraction-using-Semantic-Model-SQL-in-Microsoft-Fabric/blob/main/Pictures/graphlsql.png)

The examination uncovered that Texas, Florida, and Pennsylvania exhibit the highest levels of CO2 emissions. Notably, Texas surpasses Florida's CO2 emissions by a factor of two. This underscores the necessity for additional investigation into the root causes of elevated CO2 levels in the state of Texas
