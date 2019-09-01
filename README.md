# MSBI-Project

BI- (Business Intelligent) converting from Data into Information

Below sample project will see how we can create simple SSIS and SSAS project

## SSIS (Sql Server Integration Service)

### Lab 1 - Creating simple SSIS package

Sample SSIS project which will see Data flow and control flow in **Lab1.dtsx**<br>

Data flow - ETL activities <br>
Control flow - Non-ETL activities <br>

Step 1 - Run SQL scripts which is available in Miscellaneous <br>
Step 2 - Drag DataFlow task <br>
Step 3 - Inside this add Flat file source (to read from CSV file) -> Derived column (string manipulation) -> ADO NET Destination (insert into DB)<br>

### Lab 2 - Conditional split, Data conversion & Error handling

### Lab 3 - For loop, variables, parameters & debugging

### Lab 4 - Dimension, measures, start schema, snow flake, shared connection managers and package tasks

## SSAS
