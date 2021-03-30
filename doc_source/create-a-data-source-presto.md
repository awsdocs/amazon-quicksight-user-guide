# Creating a Data Source Using Presto<a name="create-a-data-source-presto"></a>

You can connect to a variety of databases using Amazon QuickSight as a [Presto](https://aws.amazon.com/big-data/what-is-presto/) client\. Presto processes the analytic queries on backend databases\. Then it returns results to the Amazon QuickSight client\.

The results of analytic queries run through the Presto query engine can be turned into Amazon QuickSight data sets\. You can either directly query your data through Presto, or you can import the results of your query into [SPICE](welcome.md#spice)\.

Before you use Amazon QuickSight as a Presto client to run queries, you must configure Presto for Amazon QuickSight\. 

Amazon QuickSight requires your Presto server to be secured and authenticated using Lightweight Directory Access Protocol \(LDAP\), which is available to Presto version 0\.167 or later\. If Presto is configured to allow unauthenticated access, Amazon QuickSight refuses the connection to the server\. To use Amazon QuickSight as a Presto client, you must configure LDAP authentication to work with Presto\. 

Presto's documentation contains information on how to set this up\. To start, you'll need to configure it to enable front\-end LDAP authentication over HTTPS\. For general information on Presto, see the [Presto documentation](https://prestodb.io/docs/current/)\. For information specifically on Presto and LDAP, see [Presto LDAP documentation](https://prestodb.io/docs/current/security/ldap.html)\. 

To make sure that you have configured your server for Amazon QuickSight access, follow the instructions in [Network and Database Configuration Requirements](configure-access.md)\.
