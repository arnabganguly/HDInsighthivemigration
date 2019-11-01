
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

### Upgrade the Hive 2.1.1 Metastore 

1. On the HDInsight cluster click on **Script Actions**.

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p31.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p31.png)

 2. On the Script action page populated the parameters as described below and click **Create**
    - Script Type: Custom 
    - Name: Enter a new for the script
    - Bash Script URI: ```https://hdiconfigactions.blob.core.windows.net/hivemetastoreschemaupgrade/launch-schema-upgrade.sh```
    - Node type(s): Head
    - Parameters:
       ``` SQLservername NEWSQLdbname SQLServerusername SQLServerpassword ```
       Note : Use single space with no commas or semicolons
       Example:
       ``` agclusterdbserver aghive40db username password```

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p32.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p32.png)

3. The script action starts on the cluster

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p33.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p33.png)

4. The script comes back with a green check mark which indicates successful completion. 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p34.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p34.png)

### Validate the Hive Metastore version 

After the script finishes , we would need to validate if the Hive Metastore is indeed upgraded

1. Launch the new SQL db portal(**aghive40db**) and click on **Query Editor**.You could alternatively use SSMS or Azure Data Studio. 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p35.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p35.png)

2. Enter the below query in the query editor and click Run.
``` Select * from [dbo].version```

3. Validate to see the if the schema version was upgraded to 3.1.0 . This would indicate that the Hive metastore was succesfully upgraded. 

4. Post up-gradation , delete the older HDInsight 3.6 cluster. 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p38.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p38.png)

5. In this section we upgraded the new Hive Metastore **aghive40db** from version 2.1.2 to 3.1.0 post which we deleted the older HDInsight cluster.  

6. In the next section , we could create a new HDIsnight 4.0( Hive 3.1) cluster with the new Hive Metastore and the older storage account. 

 


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1MTMwNDMyMDQsLTQwNzQzMzU4NSwxNj
MzMDc0OTM3LC0xOTg0MTc1NzUzLDIwNDAyOTc2MjJdfQ==
-->