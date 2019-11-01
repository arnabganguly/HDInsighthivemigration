
## Run TPCDS test data on the HDInsight 4.0 Hadoop cluster with Beeline CLI

Goal of this step is to run TPCDS tests with an upgraded Hive Metastore to represent regression tests of production data. 

1. The TPCDS repo should already be cloned and data should already exist from what we created earlier. 

2. Run a few TPCDS queries to represent a production regression test . Change the query number in the end to test various queries. 

```
beeline -u "jdbc:hive2://`hostname -f`:10001/tpcds_orc;transportMode=http" -n "" -p "" -i settings.hql -f queries/query12.sql
```

7. In this section we have created test data on the cluster and then tested a few queries representative of production datasets. 

8. In the next section we would upgrade the Hive Metastore from 2.1.1. to 3.1. 

[Next-->](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/UpgradeHiveMetastore.md) 


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3MzMxNzQ5M119
-->