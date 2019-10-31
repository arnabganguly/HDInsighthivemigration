## Create TPCDS test data on the HDInsight 3.6 Hadoop cluster with Beeline CLI

Goal of this step is to help generate TPCDS data with hive as a close representation of production data. 

1. Clone this repo
```
git clone https://github.com/hdinsight/tpcds-hdinsight && cd tpcds-hdinsight 
```
2. Upload the resources to DFS

```
hdfs dfs -copyFromLocal resources /tmp
```
3. Run TPCDSDataGen.hql with settings.hql file and set the required config variables.( 1 GB of data)
```
beeline -u "jdbc:hive2://`hostname -f`:10001/;transportMode=http" -n "" -p "" -i settings.hql -f TPCDSDataGen.hql -hiveconf SCALE=1 -hiveconf PARTS=1 -hiveconf LOCATION=/HiveTPCDS/ -hiveconf TPCHBIN=`grep -A 1 "fs.defaultFS" /etc/hadoop/conf/core-site.xml | grep -o "wasb[^<]*"`/tmp/resources
```
`SCALE`  is a scale factor for TPCDS. Scale factor 10 roughly generates 10 GB data, Scale factor 1000 generates 1 TB of data and so on.

`PARTS`  is a number of task to use for datagen (parrellelization). This should be set to the same value as  `SCALE`.

`LOCATION`  is the directory where the data will be stored on HDFS.

`TPCHBIN`  is where the resources are found. You can specify specific settings in settings.hql file.


4. Create tables on the generated data.

```
beeline -u "jdbc:hive2://`hostname -f`:10001/;transportMode=http" -n "" -p "" -i settings.hql -f ddl/createAllExternalTables.hql -hiveconf LOCATION=/HiveTPCDS/ -hiveconf DBNAME=tpcds
```
5. Generate ORC tables and analyze

```
beeline -u "jdbc:hive2://`hostname -f`:10001/;transportMode=http" -n "" -p "" -i settings.hql -f ddl/createAllORCTables.hql -hiveconf ORCDBNAME=tpcds_orc -hiveconf SOURCE=tpcds
beeline -u "jdbc:hive2://`hostname -f`:10001/;transportMode=http" -n "" -p "" -i settings.hql -f ddl/analyze.hql -hiveconf ORCDBNAME=tpcds_orc
```
6. Run a few queries to represent a production workload. Change the query number in the end to test various queries. 

```
beeline -u "jdbc:hive2://`hostname -f`:10001/tpcds_orc;transportMode=http" -n "" -p "" -i settings.hql -f queries/query12.sql
```

7. In this section we have created test data on the cluster and then tested a few queries representative of production datasets. 

8. In the next section we would upgrade the Hive Metastore from 2.1.1. to 3.1. 

[Next-->](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/UpgradeHiveMetastore.md) 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyNDM2MzY3NTksLTIwMDAwMzU1MjcsLT
EzNTgyMTY5NTcsNzMwOTk4MTE2XX0=
-->