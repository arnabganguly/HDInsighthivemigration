
## Create an External Metastore for the HDInsight Hadoop 3.6 cluster

1. On the Azure Portal Navigate to the SQL Database blade and click create 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p4.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p4.png)

 - 2.  Populate the  **Basics**  tab of SQL Server  with the below information.

 -   **Resource group**:  Use the same resource group used for storage

 -   **Database Details** :  
         - Database name: *Choose any allowed name for the metastore* ( I used ***aghive36db*** to represent a Hive 2.1 metastore on an HDInsight 3.6 cluster type )
         - Want to use SQL Elastic Pool : N 
         

_Enter a unique name for your storage account_
-   **Location**:  _Enter an Azure region( HDInsight cluster needs to be created in same the Azure region)_
-   **Performance**:  _Standard_
-   **Account Kind**:  _StorageV2(general purpose v2)_
-   **Replication**:  _Locally-redundant storage(LRS)_
-   **Access Tier**:  _Hot_


![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p5.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p5.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbODk1MjU3Mzk2XX0=
-->