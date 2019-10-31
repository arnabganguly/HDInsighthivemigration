

## Create a Storage account 

1. Create storage account and click create

![https://github.com/arnabganguly/llap-hdinsight/blob/master/images/Picture32.png](https://github.com/arnabganguly/llap-hdinsight/blob/master/images/Picture32.png)


2. Populate the  **Basics**  tab of Storage account with the below information.

-   **Resource group**:  _Create or use an existing resource group_
-   **Storage account name**:  _Enter a unique name for your storage account_( I used ***agstorage36*** to represent an older cluster )
-   **Location**:  _Enter an Azure region( HDInsight cluster needs to be created in same the Azure region)_
-   **Performance**:  _Standard_
-   **Account Kind**:  _StorageV2(general purpose v2)_
-   **Replication**:  _Locally-redundant storage(LRS)_
-   **Access Tier**:  _Hot_


![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p1.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p1.png)

3. Populate the  **Advanced**  tab of Storage account with the below information.

-   **Security(Secure transfer required)**:  _Enabled_
-   **Virtual Network(Allow access from)**:  _All networks_
-   **Data Protection(Blob soft delete**):  _Disabled_
-   **Data Lake Storage Gen2(Hierarchical Namespace)**:  _Disabled_


![https://github.com/arnabganguly/llap-hdinsight/blob/master/images/Picture33.png](https://github.com/arnabganguly/llap-hdinsight/blob/master/images/Picture33.png)

4. Make no changes to the Tags Tab and post validation click _Create_ on the _Review + Create_ tab to create an Azure Blob storage account.

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p2.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p2.png)





<!--stackedit_data:
eyJoaXN0b3J5IjpbODk2NzU2ODI0XX0=
-->