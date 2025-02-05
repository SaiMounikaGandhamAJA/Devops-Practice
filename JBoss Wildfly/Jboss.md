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

### Things to keep in mind before changing configurational changes :

* Where to change
* Backup
* How to change
* Try or experiment in local environment
* Documentation

## Snapshot / Backup :
for wildfly - configuration snapshot

-- > home folder of wildfly --> standalone --> configuration --> standalone_XML_History --> filename:standalone.v1

Eg: port number change 

standalone-portchange.v2

need to rename the original or existed file and then replace the customized as per requirement / change .

## Different status of the artifacts deployed in wildfly :

In wildfly deployed artifacts can have various status states including :

`Deployed:` The application is successfully running on the wildfly server and accessible to users 

`Undeployed:` The application has been removed from the server and is not currently running.

`Failed:` The deployment process encounted an error and the application is not running .

`Disabled:` The application is intentionally stopped by the administrator and cannot be accessed until enabled.

`Suspended:` The application is temporarily paused and can be resumed later .

`Redeploying:`The application is currently being with new code and is not fully available while the redeployment process is ongoing

## Accessing deplyment Status :
### Wildfly management console :
   You can view the status of deployed artifacts through the wildfly admin console , which provides a list of deployment with their current state .

   ### CLI (Command Line Interface) :
  Using the wildfly command - line interface you can query the status of deployments with management commands

* Indicating whether the application is curently running , not deployed , encountered an error during deployment , intentionally deactivated, temporarily paused or is in the process of being re-deployed with updates.

## Domain & Host Controler in wildfly :
  In jboss wildfly, a "Domain COntroller" is the central management point for a group of servers within a domain, responsible for maintaining the overall configuration and policy,
    
   while a "host controller" is a separate process running on each server within the domain,communicating with the domain controller to manage the individual server instances on that host machine;

   essentially, the domain controller dictates the overall configuration, and the host controller execute those configurations on their respective servers.

   ## Domain Controller :

   * Acts as the central management point for the entire domain.
   * Stores the domian-wide configuration in a file called "domain.xml"
   
   (home --> domain --> configuration --> domain.xml)

   * Responsible for distributed configuration changes to all host controllers within the domain.

   ## Host Controller :
   
  * Manages the application server instances running on a specific host.
  * Reads it's configuration from a "host.xml" file specific to that host.

  (home --> Domain --> configuration --> host.xml)

  * Communicates with the domain controller to receive configuration updates and start/stop server instances.