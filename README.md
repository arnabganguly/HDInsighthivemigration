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
 - The Hive Warehouse connector is used to integrate between Spark and Hive workloads. 
   

For an exhaustive overview of advancements in Hive 3.0 , listen to this [presentation](https://www.youtube.com/watch?v=exdDSckutm8) 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjEzNTE1MjAzNSwtMTA0MzcyNDExOCwtMT
I1NzIxNTI5OSwxNjQ1NzU3NDYsMTAxMDU2NTA3NCwtMTgxMjk1
Nzk1NywtNzczNTQ1NTQ0LDE0MDQ3NTc3NjksLTIwOTQ5MjE4Mz
AsLTc4OTM5ODU0LC0xOTkzNjEyMDE5LDkxODY3MDExMiwtMTg2
NjU1NjAyMCwtMTA4NTE4NjcxNiwtMjMzMDExODYsLTEzODgyOD
UxNDNdfQ==
-->