# MSBI-Project

BI- (Business Intelligent) converting from Data into Information

Below sample project will see how we can create simple SSIS and SSAS project

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

### Lab 4 - Dimension, measures, start schema, snow flake, shared connection managers and package tasks

## SSAS
