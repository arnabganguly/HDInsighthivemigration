
## Create an External Metastore for the HDInsight Hadoop 3.6 cluster

1. On the Azure Portal Navigate to the SQL Database blade and click create 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p4.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p4.png)

 2.  Populate the  **Basics**  tab of SQL Server  with the below information.

 -   **Resource group**:  Use the same resource group used for storage

 -   **Database Details** :  
           -Database name: *Choose any allowed name for the metastore* ( I used ***aghive36db*** to represent a Hive 2.1 metastore on an HDInsight 3.6 cluster type )
         - Want to use SQL Elastic Pool : N

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p5.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p5.png)

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p6.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p6.png)

 - **Compute+Storage** : Click on the *Configure Database* link  to Navigate to the database configuration page 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p7.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p7.png)

 - In the Database Configuration page select the *Standard* Tier with the below settings
    - DTU: 200
    - Data Max Size : 100 GB 
 

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyMjY4NDE2NzQsMTA0NTEzOTczNV19
-->