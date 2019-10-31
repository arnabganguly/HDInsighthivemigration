
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

 - In the Database Configuration page select the *Standard* Tier with the below settings and click *Apply* 
    - DTU: 200
    - Data Max Size : A few GBs
 
![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p8.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p8.png)

4. In the Networking tab ensure the following settings are met

 - List item

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2Mjc2NDMzNjIsMTA0NTEzOTczNV19
-->