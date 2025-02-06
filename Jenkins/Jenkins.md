## What is Continuos Integration ?
 " It is the process of automating the building and testing of code, each time one of the team member commits changes of version control"
 
 ![preview](Images/jenkins.1.PNG)

 * **CI** - Continuos Integration 
 * **CD** - Continuos Delivery / Deployment
 * First Delivery will come and then Deployment will come .

 ## Importance to Continuous Integration :

 * `Improves Quality:` Improves the quality by running multiple unit tests and analysing various static code.

 * `Increases Productivity :` Automating build of code saves a lot of time , there by increasing productivity .

 * `Reduces Risk :` Eliminate the risk of potential human errors by automating test.

## Popular Continuos Integration tools:

* **Gitlab CI**
* **Code Ship**
* **Bamboo**
* **Jenkins**
* **Team City**
* **Travis CI**
* For AWS Cloud , if we wanted to peform CI/CD, there are various services like code commit , code deploy , code guru , code build , code pipeline.

* In Azure cloud , If we want to perform CI/CD there are various services like Azure DevOps , Azure Boards, Azure Repos , Azure Pipelines,Azure testplans,Azure Artifacts.

## What is Jenkins ?
 A Continuous Integration Server which manages and control processes such as plan,code,build,test,deploy,operate,and monitor in DevOps Environment.

 ![preview](Images/jenkins.2.PNG)

## Key features of Jenkins :

* Easy Installation Process 
* Upgrades are easily available
* Provides advance security
* Light weight container support
* Optimized performance
* Distributed team management

## Why Jenkins is so popular :

* Open Source
* Good Plugin support
* Good Community support
* Fast and Reliable
* Good OS Support
* Scripted Builds

### Topics:
 Following are the topics covered in this module :

 * Jenkins Architecture
 * Plugin Management in Jenkins
 * Notification in Jenkins
 * Jenkins Master slave architecture
 * Jenkins Delivery pipeline
 * Jenkins Declarative pipeline

 ## Jenkins Architecture : Source control management :

 ![preview](Images/jenkins.3.PNG)

 ## Why do we need plugins ?
to have extra functionality

## plugin Management in Jenkins :

![preview](Images/jenkins.4.PNG)
 
 Note : In Real time , we cannot install the plugin as simple as that , reason being they might be challanges with proxy settings as well as VPN.
 
 * In order to avoid this we should configure http proxy in jenkins pluggin of advanced tab.

## How to Install Jenkins on Windows :

### Different ways of Installation :

* Using Docker 
* Using Kubernetes
* Using Linux
* Mac Os
* Windows 
* Other Systems
* War Files
* Other Servlets
* Offline Installations

### Prerequisites :

* ### Minimum Hardware Equipments :

  * 256 MB of RAM
  * 1 GB of drive space ( Although 10 GB is a recommended minimum if running jenkins as a docker container)
* ### Recommended hardware configuration for a small team :

  * 4 GB + of RAM
  * 50 GB + of drive space

Note : Jenkins tool is developed on java code.

* A system running windows 10
* The latest copy of JDK or JRE
* Access to an account with administrator
* Internet

## Install Jenkins on Windows :

* Browse to the official jenkins download page 
   
      jenkins.io/downloads

![preview](Images/jenkins.5.PNG)

* Under that downloading jenkins section is a list of installers for the long-term support (LTS) version of jenkins.

![preview](Images/jenkins.6.PNG)

* Click on windows text under download jenkins , it will start downloading

![preview](Images/jenkins.7.PNG)

* Once, you downloades the jenkins, then go for the path where you have downloaded you jenkins in your local machine.

![preview](Images/jenkins.8.PNG)

* Double click on the file , which is of type windows installer package

* The setup wizard starts-click next to proceed.

![preview](Images/jenkins.9.PNG)

* Select the install destination folder and click next to continue .

![preview](Images/jenkins.10.PNG)

* Under the run service as alocal or domain user option, enter the domain username and password for the user account you want to run jenkins with click test ceredentials to verify the login data, then click next to proceed.

Note : go for the first option which is run service as local system .

![preview](Images/jenkins.11.PNG)

* Enter the port number you want jenkins to run on. Click test port to check if the selected port is available then click next to continue .

![preview](Images/jenkins.12.PNG)

Note : default port number of Jenkins is 8080

* Select the directory where java is installed on your system and click next to proceed.


![preview](Images/jenkins.13.PNG)

* Select features you want to install with jenkins and click next to continue 

![preview](Images/jenkins.14.PNG)

* Click install to start the installation process.

![preview](Images/jenkins.15.PNG)

* Click finish after installing.

![preview](Images/jenkins.16.PNG)

## How to configure the Jenkins :

After completing the installation process , you have to unblock jenkins before you can customize and start using it.

* In your web browser , navigate to the port number you selected during the installation using the following address .

`Syntax :` http://localhost:[portnumber]

     eg: http://localhost:8080

![preview](Images/jenkins.17.PNG)

* Navigate to the location on your system specified by the unblock jenkins page

      C:\ProgramData\Jenkins\.jenkins\secrets\initialAdminPassword

![preview](Images/jenkins.18.PNG)

 Where initial admin password is a file.

 * Open the initial admin password file using a text editor such as notepad etc..

 ![preview](Images/jenkins.19.PNG)

 * Copy the password from the initial admin Password file

 ![preview](Images/jenkins.21.PNG)

 * Paste the password in the administartor password feild on the unblock jenkins page and click continue to proceed.

 ![preview](Images/jenkins.20.PNG)

## Custmize Jenkins:

* Click the install suggested plugins button to have jenkins automatically install the most frequently used plugins.

![preview](Images/jenkins.22.PNG)

* After Jenkins finishes installing the plugins, enter the required information on the create first admin user page. click save and continue to proceed.
![preview](Images/jenkins.23.PNG)

* On the Instance configuration page, confirm the port number you want jenkins to use and click save and finish to finish the initial customization.
![preview](Images/jenkins.24.PNG)

* Click start using jenkins

![preview](Images/jenkins.25.PNG)

* This is the dashboard you get after customizing jenkins :


![preview](Images/jenkins.26.PNG)

## How to stop the server jenkins on windows ?

   search --> services --> jenkins --> stop

![preview](Images/jenkins.27.PNG)

![preview](Images/jenkins.28.PNG)

## How to restart the jenkins :
 2 ways 

 1. localhost:8080/safeRestart in jenkins url

 Jenkins will try to pause jobs and restart once all running jobs are either finished or paused.

 2. localhost:8080/Restart

 * go for safeRestart only.
