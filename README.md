#  Migrate HDInsight 3.6 Hive(2.1.0) workload to HDInsight 4.0 Hive(3.1.0) 

This lab explains the steps needed to migrate multiple Hive workloads from an [HDInsight Hadoop(Hive) 3.6](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-release-notes-archive) cluster to an [HDInsight Hadoop(Hive) 4.0](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-version-release) cluster.

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
3. Run TPCDS tests to simulate Hive workloads.
4. Copy the Hive 2.1 Metastore and upgrade the Metastore copy to 3.1.
5. Delete the older HDInsight Hadoop 3.6 cluster.
6.  Create a new HDInsight 4.0 cluster with the older storage account and new upgraded 3.1 Hive Metastore.
7. Run the same TPCDS tests to ensure everything is working as intended. 

<br />

To start the lab click [NEXT->](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/CreateStorageAccount.md)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1MjY3MDc1NjcsLTE1OTE0OTI1NjIsOD
AxMTQxNTE1LDEzMjIwNzI2NzQsOTUxMDU4MTE3LC0xMDQzNzI0
MTE4LC0xMjU3MjE1Mjk5LDE2NDU3NTc0NiwxMDEwNTY1MDc0LC
0xODEyOTU3OTU3LC03NzM1NDU1NDQsMTQwNDc1Nzc2OSwtMjA5
NDkyMTgzMCwtNzg5Mzk4NTQsLTE5OTM2MTIwMTksOTE4NjcwMT
EyLC0xODY2NTU2MDIwLC0xMDg1MTg2NzE2LC0yMzMwMTE4Niwt
MTM4ODI4NTE0M119
-->