## ## Provision HDInsight Hadoop 3.6(Hive 2.1.0) cluster from Azure Management Portal

To provision HDInsight LLAP with Azure Management Portal, perform the below steps.

1.  Go to the Azure Portal portal.azure.com. Login using your azure account credentials.
    
2.  Select  **Create a resource -> Azure HDInsight -> Create**
    
3.  Click the  _Custom(size ,settings, apps) slider_
    
4.  In the  **Basics**  tab populate the following values.
    
-   **Resource Group**:_Put the cluster in the same resource group as the Storage account and Metastore_
-   **Cluster Name**:  _Enter the cluster name. A green tick will appear if the cluster name is available._
- **Region**: Choose the same region as the storage account
-   **Cluster Type**  : Cluster Type -  _Hadoop_
-  **Version**: Hadoop 2.7.3 (HDI 3.6)

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p13.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p13.png)

-   **Cluster login username**:Enter username for cluster administrator(default:admin)
-   **Cluster login password**:_Enter password for cluster login(default:sshuser)_
-   **Confirm Cluster login password**:_

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p14.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p14.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc4ODMwMTM5NCw3NzIxNDYzMjldfQ==
-->