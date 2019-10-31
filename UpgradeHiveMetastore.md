
## Upgrade the Hive Metastore from Hive 2.1.1 to Hive 3.1

### Create a copy of the Hive Metastore in HDInsight 3.6

1. From the HDInsight 3.6 cluster click on the External Metastores.

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p24.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p24.png)

2. Click on the Metastore to open the SQL DB portal.  

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p25.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p25.png)

3. On the SQL DB portal click on **Restore**. 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p26.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p26.png)

 4. In the restore blade choose the below values to get the most recent copy of the Hive Metastore 
     
 - Select Source : *Point-in-time*
 - Database name: *Assign a new db name**( I choose the name **aghive40db**)
 - Restore Point: 
    - Date: *Current date*
    -  Time: *Current time* 
  - Target Server: Choose SQL server create earlier
  - Elastic Pool: *None*
  - Pricing Tier: Same tier as older metastore db 
 Click Ok to continue with creation of a copy

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p27.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p27.png)
 
5. 


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTYzMzA3NDkzNywtMTk4NDE3NTc1MywyMD
QwMjk3NjIyXX0=
-->