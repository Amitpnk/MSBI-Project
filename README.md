# MSBI-Project

BI- (Business Intelligent) converting from Data into Information

Below sample project will see how we can create simple SSIS and SSAS project

You can refer this blog <https://amitpnk.github.io/MSBI-Project/>

## Sending feedback

For feedback can drop mail to my email address amit.naik8103@gmail.com or you can create issue

## SSIS (Sql Server Integration Service)

### Lab 1 - Creating simple SSIS package

Sample SSIS project which will see Data flow and control flow in **Lab1.dtsx**<br>

Data flow - ETL activities <br>
Control flow - Non-ETL activities <br>

*Step 1* - Run SQL scripts which is available in Miscellaneous <br>
*Step 2* - Drag DataFlow task <br>
*Step 3* - Inside this add Flat file source (to read from CSV file) -> Derived column (string manipulation) -> ADO NET Destination (insert into DB)<br>

### Lab 2 - Conditional split, Data conversion & Error handling

In **Lab2.dtsx** will see how we can create conditional split, data conversion & error handling <br>

*Step 1* - Flat file source (to read from CSV file) -> Derivied column (string manipulation) -> Data conversion (to convert into number) -> Conditional split (Based on forumla we can insert into DB or flat file destination) <br>
*Step 2* - In case of error, we can redirect into log file (using flat file destination)

### Lab 3 - For loop, variables & parameters

In **Lab3.dtsx** will see how we can extract dynamically with multiple csv files using for loop and variables/parameters 

*Step 1* - From previous Lab drag *For loop container* and inside this add *Data flow task* <br>
*Step 2* - Open package *variales* and add variable *FullFilePath* <br>
*Step 3* - Right click on Foreach loop container and go to Edit -> Collection -> Enumerator <br>
&emsp;&emsp;&emsp;- Modify *ForEach file enumator* <br>
&emsp;&emsp;&emsp;- Modify *Folder path source*<br>
&emsp;&emsp;&emsp;- Modify **.txt*<br>
&emsp;&emsp;&emsp;- Modify *Fully qualified*<br>
*Step 4* - Go to Variable Mapping <br>
&emsp;&emsp;&emsp;- Add variable *User::FullFilePath*<br>
*Step 5* - Go to properties of Flat file connection manager (csv connection) -> Expression -> add connectionString to *@User:FullFilePath*<br>
*Step 6* - Incase of parameter : go to Parameter tab -> setValue and right click on *ForEach loop container* -> Expression -> Directory - *$Package:ParamFilePath* <br>

### Lab 4 - Dimension, measures, start schema, snow flake, shared connection managers and package tasks

There is mainly 2 category of tables <br>
* **Measures/Facts** - Is numerical property
* **Dimensions** -  Context of Measures

Eg: Sales Amount as per country, year and product
here Sales Amount is *Measures* and Country is *Dimensions*

Star schema - Fact is central table with foreign key relationship with dimension
Snow flake - Same as Star schema and also dimension table also connected

*Step 1* - Create new SSIS package as *Country.dtsx*, *States.dtsx*, *SalesPerson.dtsx*, *Product.dtsx*  and in DataFlow task create FlatFileSource-> ADO NET Destination in each file w.r.t country, states, salesPersion & product csv file <br>
*Step 2* - Create Global connection string and map to each file instead of creating individual file <br>
*Step 3* - Create *Main.dtsx* and add control *ExectuePackageTask* and map to each dtsx file mentioned in step 1 <br>

### Lab 5 - SCD (Slowly changing dimension), Type 0, Type 1, OLE DB command and Unicode conversions


## SSAS
