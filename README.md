#  Upgrade from HDInsight 3.6 Hive(2.1.0) cluster to HDInsight 4.0 Hive(3.1.0) cluster 

This lab explains the steps needed to upgrade from an [HDInsight Hadoop(Hive) 3.6](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-release-notes-archive) cluster to an [HDInsight Hadoop(Hive) 4.0](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-version-release) cluster.

HDInsight 4.0 brings [upgraded versions for all Apache components](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-component-versioning) , but for this lab we specifically focus on the Hive versions. 

|Component| HDInsight 4.0 | HDInsight 3.6 |
|--|--|--|
|Hive| 3.1.0 |2.1.0 ; 1.2.1| 

Some key areas that Hive 3.x differs from earlier versions are.

 **Client** 

 - Hive CLI support is deprecated in Hive 3.x and only the thin client
   Beeline is supported

**Transaction Processing** 

 - ACID tables are the default table type in Hive 3.x with performance as good as non Acid
 - Automatic query cache

 **Catalogs** 

 - Spark and Hive use independent catalogues for Spark SQL or Hive tables in same or independent clusters
 - The [Hive Warehouse connector](https://docs.microsoft.com/en-us/azure/hdinsight/interactive-query/apache-hive-warehouse-connector) is used to integrate between Spark and Hive workloads. 
   

For an exhaustive overview of advancements in Hive 3.0 , listen to this [presentation](https://www.youtube.com/watch?v=exdDSckutm8) 

## Lab

This lab is a simulation of a real migration and will consist of the following steps in sequence.  

1. Create an HDInsight Hadoop 3.6 cluster.
2. Create test data in the HDInsight 3.6 cluster. We use TPCDS data here. 
3. Run a TPCDS tests to see if everything is working as intended.
4. Copy the Hive 2.1 metastore and upgrade the metastore to 3.1.
5. Delete the older HDInsight Hadoop 3.6 cluster.
6.  Create a new HDInsight 4.0 cluster with the older storage account and upgraded 3.1 metastore.
7. Run the same TPCDS tests to ensure everything is working as intended. 


To start the lab click [NEXT->](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/CreateStorageAccount.md)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1ODE5NTI4ODgsMTMyMjA3MjY3NCw5NT
EwNTgxMTcsLTEwNDM3MjQxMTgsLTEyNTcyMTUyOTksMTY0NTc1
NzQ2LDEwMTA1NjUwNzQsLTE4MTI5NTc5NTcsLTc3MzU0NTU0NC
wxNDA0NzU3NzY5LC0yMDk0OTIxODMwLC03ODkzOTg1NCwtMTk5
MzYxMjAxOSw5MTg2NzAxMTIsLTE4NjY1NTYwMjAsLTEwODUxOD
Y3MTYsLTIzMzAxMTg2LC0xMzg4Mjg1MTQzXX0=
-->