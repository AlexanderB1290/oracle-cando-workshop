![](../common/images/customer.logo.png)
---
# ORACLE CanDo Workshop #

## Create Java Cloud Service instance using user interface ##

### Introduction ###

By using Oracle Java Cloud Service, you can quickly create and configure an Oracle WebLogic Server domain and set up your Java EE application environment without worrying about setting up any infrastructure or platform details yourself. All Oracle Java Cloud Service instances that you create are also preconfigured to use your database deployment in Oracle Database Cloud Service, and an object storage container that you create in your Oracle Storage Cloud Service.

### About this tutorial ###
This tutorial demonstrates how to:
	
+ create Java Cloud Service using the user interface.

### Prerequisites ###

+ Oracle Public Cloud Service account including Java, Database and Storage Cloud Service
+ Oracle Java Cloud Service uses Oracle Database Cloud Service to host the Oracle Fusion Middleware component schemas required by Oracle Java Required Files (JRF). Prior to creating an Oracle Java Cloud Service instance, [use your Oracle Database Cloud Service subscription to create a database deployment](../dbcs-create/README.md). As part of the instance creation process, Oracle Java Cloud Service provisions this database deployment with the Oracle JRF schemas.

###Create a Java Cloud Service instance###

With the help of the Oracle documentation [Creating an Oracle Java Cloud Service Instance](http://docs.oracle.com/en/cloud/paas/java-cloud/jscug/creating-oracle-java-cloud-service-instance.html), provision a Java Cloud Service instance with the following details below:

*NOTE: feel free to modify the details by will, but don't forget to note and remember your custom settings!*

 - **Service Name:**  the name of your service instance, e.g. techco
Select subscription type. 
 - **Description:** (Optional) Enter a short description of the Oracle Java Cloud Service instance
 - **Service Level:** Oracle Java Cloud Service
 - **Metering Frequency:** Monthly
 - **Service Release:** Select the latest 12c Release available
 - **Service Edition:** Enterprise Edition
 - **Compute Shape:** number of OCPU and size of the RAM. Choose the smallest (default) one.
 - **SSH Public Key:** public key which will be uploaded to the VM during the creation. It allows to connect to the VM through ssh connection using the private key. You can create a new one, although it's better to use the same publicKey what was generated for Database Cloud Service instance. Click on Edit button and select the previously saved (during the Database Cloud Service creation) *GIT_REPO_LOCAL_CLONE/cloud-utils/publicKey*. You can also copy the content of publicKey into Key Value field. If you don't have or want to to create different keypair select Create a New Key option and download the newly generated keypair for later usage. 
 - **Cluster Size:** to save resources leave the default 1. Which means one managed server
 - **Domain Partitions:** Create mutitenant instance. Select 1 to enable partitioning
 - **Local Administrator Username:**  the username for the WebLogic Administrator. You can change the user name through the WebLogic Server Administration Console after the service instance is provisioned.
 - **Password:** WebLogic administrator's password. Don't forget to note the provided password.
 - **Enable access to Administration Consoles:** check this to get access to the Admin console.
 - **Deploy Sample Application:** check it to deploy the sample application. It can be useful to test accessibility (correct LB configuration, etc.) of the Java Cloud Service Instance.
 - **Do not create and configure a Coherence Data Tier** - just to save time and resources.
 - **Database Configuration** for For Oracle Required Schema
	 - **Name:** Database Cloud Service name to store WebLogic repository data. Select from the list your database service instance cteated during the Database Cloud Service creation
	 - **PDB Name:** pluggable database service identifier of the Database Cloud Service instance which will be used to store repository schema. If you have choosen default (PDB1) during Database Cloud Service creation then leave the default here too
	 - **Administrator Username:** DBA admin to create repository schema for Java Cloud Service instance. Enter: **sys**
	 - **Password:** DBA admin password you provided during Database Cloud Service creation.
	 - **For Application Schema:** do not Add
 - **Provision Load Balancer:** to save resources for sample application we will not create Load Balancer instance. Leave default: **No**
 - **Cloud Storage Container:** the name of the container used to provide storage for your service instance backups. The format is the following: Storage-IDENTITYDOMAIN/CONTAINERNAME. The container don't need to be created in advance, because -see below- there is an option to create automatically. 
 - **Cloud Storage User Name and Password:**  the credentials for storage. Usually it is the same what was used to sign in to Oracle Cloud Services.
 - **Create Cloud Storage Containers:** if the container defined above does not exist then check this

The final page is the summary page about the configuration before submit the instance creation request. Click **Create** to start the provisioning of the new service instance.

When the request has been accepted the Java Cloud Service Console page appears and shows the new instance. The instance now is in Maintenance (Progress) mode. Click ***In Progress*** link to get more information about the status.


