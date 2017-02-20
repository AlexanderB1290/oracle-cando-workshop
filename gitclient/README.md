![](../common/images/customer.logo.png)
---
# ORACLE CanDo Workshop #
-----
## Continuous build integration using Git client with Oracle Developer Cloud Service and Application Container Cloud Service ##

### About this tutorial ###
Besides using Eclipse for your project, you can use any favourite Text editor and Git tool to create and modify your project and then push the code to Developer Cloud Service remote repository.

This tutorial shows how to use a Git client with Oracle Developer Cloud Service and Application Container Cloud Service.

### Prerequisites ###

- You have [created and deployed a SpringBoot Microservice with Developer Cloud Service & Application Container Cloud Service](../springboot-sample/README.md)
- You have configured a Build for the springboot-sample app based on SCM polling schedule
- (Optional) You have configured a Deploy configuration with Automatic deployment of springboot-sample app to Application Container Cloud Service 
- (Optional) You are familiar how to use the [Agile Methodology in Oracle Developer Cloud Service](../agile/README.md) 

----

### Continuous build integration using Git client with Oracle Developer Cloud Service and Application Container Cloud Service ###

-

#### JSE microservice sample ####

Sign in to [https://cloud.oracle.com/sign-in](https://cloud.oracle.com/sign-in). Select your datacenter, then provide the identity domain and credentials. After a successful login, on your Dashboard, click on Developer Cloud Service name and then click **Open Service Console**.

Log in to Oracle Developer Cloud Service and open your **springboot-sample** project.

During the steps below you can apply Agile methodology in Developer Cloud Service according to your activities on the springboot-sample project.

On your springboot-sample project, in the Project page, within the REPOSITORIES section, copy the URL of your springboot-sample.git repo from the HTTP text-box. It should be something similar to: `https://{yourDevCSProjectURI}/springboot-sample.git` 

Clone your DevCS springboot-sample.git repository to your local machine by using your favourite Git tool. 
For example, you can download and install [Git](https://git-scm.com/downloads)

Below is an example with Git bash:

`cd {path_to_your_local_Git_repo_folder}`		
`git clone https://{YourDevCSProjectURI}/springboot-sample.git `

Make some changes in the code by using your favourite code editor (eg. Brackets, Atom, Notepad++ etc.). For example, edit the file:
`src\main\webapp\WEB-INF\views\welcome.jsp`

Push changes to the Developer Cloud Service remote springboot-sample repo (master). 
Below is an example with Git bash:

`git commit -am "Edited welcome.jsp page"`		
`git push -u origin master`

On your springboot-sample project in Developer Cloud Service, observe the results in Build and Deploy pages.

For additional samples about JSE microservices refer the Tutorials section on the Oracle Application Container Cloud Service Documentation [Create Sample Java SE Applications](http://docs.oracle.com/en/cloud/paas/app-container-cloud/create-sample-java-se-applications.html)

-

#### Node.js microservice sample ####

Sign in to [https://cloud.oracle.com/sign-in](https://cloud.oracle.com/sign-in). Select your datacenter, then provide the identity domain and credentials. After a successful login, on your Dashboard, click on Developer Cloud Service name and then click **Open Service Console**.

Log in to Oracle Developer Cloud Service and create a new **node-sample** project based on Initial Repository.

Clone your DevCS **node-sample.git** repository to your local machine by using your favourite Git tool. 

Access the Tutorials section on the Oracle Application Container Cloud Service Documentation [Create Sample Node.js Applications](http://docs.oracle.com/en/cloud/paas/app-container-cloud/create-sample-node.js-applications.html)

For example, select the Tutorial [Developing a RESTful Node.js and HTML5 application to Oracle Application Container Cloud Service](http://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/apaas/node-basicRest/nodecloud-REST.html#overview) and either:
+ start developing the RESTful project source code in your local Git repo
+ or download the RESTful-project.zip  with the completed project and unzip it into your local Git repo

In you local Git, commit and push the changes to the remote DevCS **node-sample.git**. 
In Dev CS, as you did for the *springboot-sample* project, do the Build. 
*Tip:* Into the Build Steps tab, click Add Build Step, and select `Execute shell`. For Command enter `npm install`. Into the Post Build tab, check Archive the artifacts and enter `**/target/*` for Files to Archive. 
Then do the Deploy on ACCS and access the app on ACCS.

-

#### PHP microservice sample ####

Sign in to [https://cloud.oracle.com/sign-in](https://cloud.oracle.com/sign-in). Select your datacenter, then provide the identity domain and credentials. After a successful login, on your Dashboard, click on Developer Cloud Service name and then click **Open Service Console**.

Log in to Oracle Developer Cloud Service and create a new **php-sample** project based on Initial Repository.

Clone your DevCS **php-sample.git** repository to your local machine by using your favourite Git tool. 

Access the Tutorials section on the Oracle Application Container Cloud Service Documentation [Create Sample PHP Applications](http://docs.oracle.com/en/cloud/paas/app-container-cloud/create-sample-php-applications.html)

For example, select the Tutorial [Oracle Application Container Cloud Service: Building a RESTful API with PHP](http://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/apaas/php/php-employees-service/php-employees-service.html) and either:
+ start developing the PHP REST API project source code in your local Git repo
+ or download the phpEmployeeAPI.zip with the completed project and unzip it into your local Git repo

In you local Git, commit and push the changes to the remote DevCS **php-sample.git**. 

In Dev CS, as you did for the *springboot-sample* project, do the Build.
*Tip:* Into the Build Steps tab, click Add Build Step, and select `Execute shell`. For Command enter: `zip -j php-sample.zip`. Into the Post Build tab, check Archive the artifacts and enter `*.zip` for Files to Archive. 

On the [Oracle Application Container Cloud Service: Building a RESTful API with PHP](http://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/apaas/php/php-employees-service/php-employees-service.html) page, continue with the section `Setting Up the Database and the Objects`

Then deploy the **php-sample** on ACCS either:
+ by using Deploy on DevCS 
+ or by using the ACCS UI console - on the [Oracle Application Container Cloud Service: Building a RESTful API with PHP](http://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/apaas/php/php-employees-service/php-employees-service.html) page, follow the instructions in the `Deploying the Application to Oracle Application Container Cloud Service` section

Then back on the [Oracle Application Container Cloud Service: Building a RESTful API with PHP](http://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/apaas/php/php-employees-service/php-employees-service.html) page, continue with the section `Adding the Database Service Binding` and `Testing the REST Service`.
