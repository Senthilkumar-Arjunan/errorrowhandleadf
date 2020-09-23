# errorrowhandleadf
Copying correct and corrpted records from Blob to Azure SQL DB using ADF
======================================================================

Steps followed
==============
1.Created Dataflow
2.Created 3 datasets
    *) BlobDataset
    *) CorrectRowDBDataSet
    *)ErrorRowDBDataSet
3.Configured Source as Blob storage
4.Created 2 conditional split (ErrorRows & GoodRows)
5.Created DerivedColumn (For adding new column, It should take filename as the value and also convered date column data type)
6.Created two sinks, Sink datasets are having two different AZURE SQL tables (TB, TB_Bad)
7.If we click the publish, good records are moving into TB table & bad/corrupted records are moving into TB_Bad tables

Services used
=============

Azure Blob storage
Azure SQL DB
ADF
