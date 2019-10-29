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

 **Catalogs** 

 - Spark and Hive use independent catalogues for Spark SQL or Hive
   tables in same or independent clusters

 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTY0NTc1NzQ2LDEwMTA1NjUwNzQsLTE4MT
I5NTc5NTcsLTc3MzU0NTU0NCwxNDA0NzU3NzY5LC0yMDk0OTIx
ODMwLC03ODkzOTg1NCwtMTk5MzYxMjAxOSw5MTg2NzAxMTIsLT
E4NjY1NTYwMjAsLTEwODUxODY3MTYsLTIzMzAxMTg2LC0xMzg4
Mjg1MTQzXX0=
-->