
## Run TPCDS test data on the HDInsight 4.0 Hadoop cluster with Beeline CLI

Goal of this step is to run TPCDS tests with an upgraded Hive Metastore to represent  regression tests of Hive workloads. 

1. The TPCDS repo should already be cloned and TPCDS data should already exist from what we created earlier. 

2. SSH into the cluster using the ssh credentials provided durinng cluster creation. 

3. Run a few TPCDS queries to represent a production regression test . Change the query number in the end to test various queries. 

```
beeline -u "jdbc:hive2://`hostname -f`:10001/tpcds_orc;transportMode=http" -n "" -p "" -i settings.hql -f queries/query12.sql
```

4. In this lab we migrated multiple HDInsight 3.6 Hive workloads to HDInsight 4.0. 


>**Further reference:**
 - [Migrate Azure HDInsight 3.6 Hive workloads to HDInsight 4.0](https://docs.microsoft.com/en-us/azure/hdinsight/interactive-query/apache-hive-migrate-workloads)
 - [Whats new in Hive 3.0](https://docs.cloudera.com/HDPDocuments/HDP3/HDP-3.1.4/hive-overview/content/hive_whats_new_in_this_release_hive.html)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMzczNzkzMTgxLC0xNjI0ODY0NzJdfQ==
-->