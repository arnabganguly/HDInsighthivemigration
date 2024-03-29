## Provision HDInsight Hadoop 4.0(Hive 3.1.0) cluster from Azure Management Portal

To provision HDInsight LLAP with Azure Management Portal, perform the below steps.
<br />
1.  Go to the Azure Portal portal.azure.com. Login using your azure account credentials.
    
2.  Select  **Create a resource -> Azure HDInsight -> Create**
    
3.  Click the  _Custom(size ,settings, apps) slider_
    
4.  In the  **Basics**  tab populate the following values.
    
-   **Resource Group**:_Put the cluster in the same resource group as the Storage account and Metastore_
-   **Cluster Name**:  _Enter the cluster name. A green tick will appear if the cluster name is available._
- **Region**: Choose the same region as the storage account
-   **Cluster Type**  : Cluster Type -  _Hadoop_
-  **Version**: Hadoop 3.1.0(HDI 4.0)

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p40.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p40.png)

-   **Cluster login username**:Enter username for cluster administrator(default:admin)
-   **Cluster login password**:_Enter password for cluster login(admin)_
-   **Confirm Cluster login password**:_Repeat the same password as used earlier_
- **Secure Shell(SSH) username**:_Enter the SSH username for the cluster(default:sshuser)
- **Use cluster login for SSH**: *Check this box(this makes your SSH password same as the cluster admin password)*

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p41.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p41.png)

5. In the  **Storage**  tab populate the following values.

-   **Primary Storage Type**:  _Azure Storage_
- **Selection method**: Select from list
-   **Primary Storage account**: Select the Azure storage blob account created earlier.
- **Container**: Enter the same storage container that was used for the previous HDInsight 3.6 cluster

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p42.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p42.png)

- **Metastore Settings**: Enter the name for the new SQL Database/SQL Server(**agclusterdbserver/aghive40db**) combination that was upgraded in the last step 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p43.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p43.png)


6. Click Authenticate to enter the username and password for the Metastore. Enter the username and password that was set for the SQL Server. 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p44.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p44.png)

 7. In the *Configuration+Pricing* tab select the node sizes for the cluster. There are no hard and fast rules and the recommendation is to select larger nodes for faster data processing. Note that choosing nodes that are too small may result in failures. 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p45.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p45.png)

8. In the *Review+Create* tab , review the cluster specifics and click **Create**.

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p46.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p46.png) 

9. In this step we created an HDInsight 4.0 Hadoop cluster with preconfigured upgraded external metastore and mapped its storage to a preexisting storage container. 
 
10. In the next step we will create some test data in the cluster to represent a production workload. 
<br />

[NEXT->](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/CreateTestData1.md)



<!--stackedit_data:
eyJoaXN0b3J5IjpbOTM4NTU3NTBdfQ==
-->