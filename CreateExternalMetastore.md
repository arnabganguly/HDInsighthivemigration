
## Create an External Metastore for the HDInsight Hadoop 3.6 cluster

1. On the Azure Portal Navigate to the SQL Database blade and click create 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p4.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p4.png)

 2.  Populate the  **Basics**  tab of SQL Server  with the below information.

 -   **Resource group**:  Use the same resource group used for storage

 -   **Database Details** :  
       - Database name: *Choose any allowed name for the metastore* ( I used ***aghive36db*** to represent a Hive 2.1 metastore on an HDInsight 3.6 cluster type 
        - Server :- Click *Create new*
            - Server admin login: Create a username
             - Password/Confirm Password : Enter Metastore server password 
              - Location : Choose same location as Storage Account 
               
        - Want to use SQL Elastic Pool : N


![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p5.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p5.png)

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p6.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p6.png)

 - **Compute+Storage** : Click on the *Configure Database* link  to Navigate to the database configuration page 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p7.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p7.png)

4. In the Database Configuration page select the *Standard* Tier with the below settings and click *Apply* 
    - DTU: 200
    - Data Max Size : A few GBs
 
![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p8.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p8.png)

 5. In the Networking tab ensure the following settings are met

 - Connectivity Method : Public endpoint
 - Firewall Rules:
    - *Allow Azure Services and Resources to Access this Server* : Yes
    - *Add current IP address*: Yes 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p9.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p9.png)

6. Leave the *Additional settings* and *Tags* to their default state

7.  In the *Review+Create* tab click *Create*

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p10.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p10.png) 
   
8. In this section we created an External Hive Metastore(**aghive36db**) which we will use subsequently in an HDInsight 3.6 cluster. 

![https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p11.png](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/images/p11.png)
<br />

[Next->](https://github.com/arnabganguly/HDInsighthivemigration/blob/master/CreateHDInsight36cluster.md) 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQwNDE3ODYwOCwtOTgzNjYyNTUxXX0=
-->