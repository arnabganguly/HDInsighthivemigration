
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
3. Run TPCDSDataGen.hql with settings.hql file and set the required config variables.
```
beeline -u "jdbc:hive2://`hostname -f`:10001/;transportMode=http" -n "" -p "" -i settings.hql -f TPCDSDataGen.hql -hiveconf SCALE=1 -hiveconf PARTS=1 -hiveconf LOCATION=/HiveTPCDS/ -hiveconf TPCHBIN=`grep -A 1 "fs.defaultFS" /etc/hadoop/conf/core-site.xml | grep -o "wasb[^<]*"`/tmp/resources


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTkyODU5NDYzMSw3MzA5OTgxMTZdfQ==
-->