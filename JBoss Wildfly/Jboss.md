## Web Server - JBoss Wildfly

Jboss is a powerful open source java application server developed by Redhat.

* In jobass we are having 2 port numbers that is 9990 is for admin and 8080 for access applications.

Syntax : 
  
   `admin :`   url:9990> (for admin it asks username and Password)
   
   `Accessing Application :` url:8080>/artifact-name
    
* To download the jboss we need to go for 
     
     
      wildfly.org/downloads
* Current version of jboss is 35

## Folder Structure :

* Domain
* Modules
* Welcome-content
* docs
* bin
* Applicant

* To start the jboss server , we need to for home folder of the jboss then go for bin , then standalone (Batch file)
 home folder of jboss --> bin --> standalone (Batch file)

 ## How to create management console user ?

  home folder --> bin --> add -user (Windows batch file )
  
  * Once we double click on the file , it will open command prompt and ask us what type of user do you wish to add ?
   
   a ) management user
   
   b ) application user
 choose option a and click on enter
  
  after it will ask us to give username after giving username it will ask us to give password , after giving password it asks us to re-enter the password .
  
  * one of the folder in jboss is standalone where we are having the configuration , deployment , logs folders

  * `Conf :` where we will be having configurations of applications , users specifies 
  Eg : mgmt-users.properties & mgmt-groups.properties

  * `Logs :`  standalone --> log --> logs of the wildfly

  * `Deployment :` A deployment represents anything that can be deployed 9eg : an application such as EJB-JAR , WAR , EAR , any kind of standard archive such as RAR or JBOSS - Specific deployment ) into a server .
  * You can use drag and drop to add new content or replace existing deployment simply drag one or several files into the deployment column .
  * if there's already a deployment with the same name , the deployment will be replaced , otherwise the deployment will be added . 
  * The deployments added by drag and drop will be enabled by default .
  * When we click on plus symbol, left side where we can see upload deployment , unmanaged deployment , 

  ## How to deploy application (or) artifacts in wildfly ?
  1. Copying the war file and pasting it in deployment folder of wildfly (Home of the wildfly --> standalone --> deployment)

  (or) 

cp artifact source path> destination of deployment of wildfly>

2. Jboss wildfly GUI --> upload artifact .