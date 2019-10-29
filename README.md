#  Upgrade from HDInsight 3.6 Hive(2.1.0) cluster to HDInsight 4.0 Hive(3.1.0) cluster 

This lab explains the steps needed to upgrade from an HDInsight Hadoop(Hive) 3.6 cluster to HDInsight Hadoop(Hive) 4.0 cluster.

HDInsight 4.0 brings upgraded versions for all Apache components , but for this lab we specifically focus on the Hive versions. 

|Component| HDInsight 4.0 | HDInsight 3.6 |
|--|--|--|
|Hive| 3.1.0 |2.1.0 ; 1.2.1| 

Some key areas that Hive 3.x differs from earlier versions are.

 **Client** 

 - Hive CLI support is deprecated in Hive 3.x and only the thin client
   Beeline is supported

**Transaction Processing** 

 - ACID tables are the default table type in Hive 3.x
 - Automatic query cache
 - Materilized views 

 **Catalogs** : Spark and Hive use independent catalogues for Spark SQL or Hive tables in same or independent clusters
 

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyODcwMTQ0NjQsMTAxMDU2NTA3NCwtMT
gxMjk1Nzk1NywtNzczNTQ1NTQ0LDE0MDQ3NTc3NjksLTIwOTQ5
MjE4MzAsLTc4OTM5ODU0LC0xOTkzNjEyMDE5LDkxODY3MDExMi
wtMTg2NjU1NjAyMCwtMTA4NTE4NjcxNiwtMjMzMDExODYsLTEz
ODgyODUxNDNdfQ==
-->