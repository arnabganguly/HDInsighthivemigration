
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
 
 Click **OK** to continue with creation of a copy

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p27.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p27.png)
 
5. After creation, the new SQL db(**aghive40db**) appears as an additional database in the same SQL Server.

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p28.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p28.png)

6. On the HDInsight cluster click on **Script Actions**.

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p31.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p31.png)

 7. On the Script action page populated the parameters as described below
    - Script Type: Custom 

 

 


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExMDU5Mjc2OCwxNjMzMDc0OTM3LC0xOT
g0MTc1NzUzLDIwNDAyOTc2MjJdfQ==
-->