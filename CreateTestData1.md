
## Run TPCDS test data on the HDInsight 4.0 Hadoop cluster with Beeline CLI

Goal of this step is to run TPCDS tests with an upgraded Hive Metastore to represent  regression tests of Hive workloads. 

1. The TPCDS repo should already be cloned and TPCDS data should already exist from what we created earlier. 

2. Run a few TPCDS queries to represent a production regression test . Change the query number in the end to test various queries. 

```
beeline -u "jdbc:hive2://`hostname -f`:10001/tpcds_orc;transportMode=http" -n "" -p "" -i settings.hql -f queries/query12.sql
```

7. In this section we have ran the same TPCDS tests on an upgraded HDInsight 4.0 cluster with a Hive 3.1 Metastore  ,representative of production regression test. 

8. In this lab we migrated a HDInsight 3.6 Hive worloads to  HDIsnight 4.0. 

[Next-->](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/UpgradeHiveMetastore.md) 


<!--stackedit_data:
eyJoaXN0b3J5IjpbMzIyNDE1NjY0XX0=
-->