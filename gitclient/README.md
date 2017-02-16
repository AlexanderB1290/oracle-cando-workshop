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

#### Continuous build integration using Git client with Oracle Developer Cloud Service and Application Container Cloud Service ####

Sign in to [https://cloud.oracle.com/sign-in](https://cloud.oracle.com/sign-in). Select your datacenter, then provide the identity domain and credentials. After a successful login, on your Dashboard, click on Developer Cloud Service name and then click **Open Service Console**.

Log in to Oracle Developer Cloud Service and open your **springboot-sample** project.

During the steps below you can play and improvise with Agile methodology in Developer Cloud Service according to your activities on the springboot-sample project.

On your springboot-sample project, in the Project page, within the REPOSITORIES section, copy the URL of your springboot-sample.git repo from the HTTP text-box. It should be something similar to: `https://{yourDevCSProjectURI}/springboot-sample.git` 

Clone your DevCS springboot-sample.git Git repository to your local machine by using your favourite Git tool. 
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

---

For additional samples about JSE, Node.JS and PHP microservices, refer the Tutorials section on the [Oracle Application Container Cloud Service Documentation](http://docs.oracle.com/en/cloud/paas/app-container-cloud/index.html)


