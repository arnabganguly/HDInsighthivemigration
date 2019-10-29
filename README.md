#  Upgrade from HDInsight 3.6 Hive(2.1.0) cluster to HDInsight 4.0 Hive(3.1.0) cluster 

This lab explains the steps needed to upgrade from an HDInsight Hadoop(Hive) 3.6 cluster to HDInsight Hadoop(Hive) 4.0 cluster.

HDInsight 4.0 brings upgraded versions for all Apache components , but for this lab we specifically focus on the Hive versions. 

|Component| HDInsight 4.0 | HDInsight 3.6 |
|--|--|--|
|Hive| 3.1.0 |2.1.0 ; 1.2.1| 

Some key areas that Hive 3.x differs from earlier versions are.

 **Client** : Hive CLI support is deprecated in Hive 3.x and only the thin client Beeline is supported 
**Transaction Processing**: ACID tables are the default table type in Hive 3.x
 **Metastore** : 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA5MTE3MTQ4MywxMDEwNTY1MDc0LC0xOD
EyOTU3OTU3LC03NzM1NDU1NDQsMTQwNDc1Nzc2OSwtMjA5NDky
MTgzMCwtNzg5Mzk4NTQsLTE5OTM2MTIwMTksOTE4NjcwMTEyLC
0xODY2NTU2MDIwLC0xMDg1MTg2NzE2LC0yMzMwMTE4NiwtMTM4
ODI4NTE0M119
-->