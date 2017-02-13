![](common/images/customer.logo.png)
---
# ORACLE CanDo Workshop #

## Introduction ##

Oracle Cloud is the industry’s broadest and most integrated public cloud. It offers best-in-class services across software as a service (SaaS), platform as a service (PaaS), and infrastructure as a service (IaaS), and even lets you put Oracle Cloud in your own data center. Oracle Cloud helps organizations drive innovation and business transformation by increasing business agility, lowering costs, and reducing IT complexity. The workshop content shows different aspects of Application Development in the cloud with different set of Oracle Cloud Services.

### Prerequisites for Hands-on Tutorials ###

The workshop is intended to work with an Oracle PaaS trial account. To get an account look into [here](common/request.for.trial.md). When [Sign In to Oracle Cloud](common/sign.in.to.oracle.cloud.md) get your account details ready to replace the values below with yours when it is required:

+ Oracle Cloud account **username** and **password**
+ Oracle Cloud **identity domain**
+ **Data center/region**

NOTE: Before you start to use your new Oracle Public Cloud services make sure that the replication policy has been set for your account. Otherwise you can not create storage container which is necessary for most of the services. See [Selecting a Replication Policy for Oracle Storage Cloud Service](https://docs.oracle.com/en/cloud/iaas/storage-cloud/cssto/selecting-replication-policy-your-service-instance.html).

### Important ###

During the hands-on execution you will create several public cloud service instances what will be available on the world wide web. Even if these instances are for demo purposes keep in mind it is not a best practice to use weak or known (stored here in the tutorial) passwords especially in such open environment. Thus this workshop content does not recommend any password so you need to define those. You will be asked to provide password at certain points and please remember them  for  later usage.

The content contains several independent modules that cover different aspects of the application development in the Oracle Cloud. These modules could be executed independently unless you find in the Prerequisites that they are dependent on each other.

----

## List of Hands-on Tutorials ##


#### Continuous Integration, Continuous Delivery and Microservices with Oracle Developer Cloud Service, Oracle Application Container Cloud Service, Eclipse and Git ####

+ [Create and Deploy a SpringBoot Microservice with Developer Cloud Service & Application Container Cloud Service](springboot-sample/README.md)
+ [Using the Agile Methodology in Oracle Developer Cloud Service](agile/README.md)
+ [Continuous build integration using Eclipse with Developer Cloud Service & Application Container Cloud Service](oepe/README.md)
+ [Continuous build integration using Git client with Developer Cloud Service & Application Container Cloud Service](gitclient/README.md)


#### Deploy Java EE application to Oracle Java Cloud Service ####

+ [Create Database Cloud Service Instance using user interface](dbcs-create/README.md)
+ [Create Java Cloud Service Instance using user interface](jcs-create/README.md)
+ [Prepare Database Cloud Service Instance to store sample application's data](dbcs-prepare/README.md)
+ [Deploy Java EE sample application to Oracle Java Cloud Service using Admin console](jcs-deploy/README.md)


#### Migrate WebLogic 10.3.6 (on premise) Application to Java Cloud Service with App2Cloud tool ####

+ [Migrate Weblogic 10.3.6 (on premise) Application to Java Cloud Service with App2Cloud tool](app-2-cloud/README.md)


---

## [License](LICENSE.md)
Copyright (c) 2014, 2016 Oracle and/or its affiliates
The Universal Permissive License (UPL), Version 1.0
