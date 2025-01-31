# `Apache Tomcat :`
 apache Tomcat is an open - source web-server and servlet container for java code .

 ## `Prerequisites :`
  * Java JRE installed and configured 
  * O.S
  * Network
  * Administration Privillage

## `Installation of Tomcat on Windows :`

* **Step 1:** Download  Tomcat for Windows
   * Browse the official Apache tomcat website . Locate the download section and click the latest version available
* **Step 2:** Install Tomcat
   * Install  Tomcat via the windows servise install for an automated and wizard guided experience .
   * After downloading the 32 bit / 64 bit windows zip file , depending on your windows version , unzip the downloaded file . Right - click the file and select extract all .
   * Navigate to unzip file of the apache tomcat


  `Default Port number of the tomcat is 8080. ` if at all we want to change the default port number , we need to go to 
  
  **Apache tomcat --> config --> server xml.**
   
      Connector port ="8080" protocol = "HTTP 1.1"
   
      Connection Timeout = "20000"
   
      redirect port = "8443"/>
    
    Change the connector port number to any number between 1024 and 655535 .

`How to start and stop the Apache Tomcat ?`
 
 ### To Start :
 
 Apache Tomcat --> bin --> Startup ( Windows Batch File) 

 ### To Stop :

 Apache Tomcat --> bin --> Shutdown ( Windowsbatch file )

 ### For configuration Changes :

 Apache Tomcat --> Conf

 ### For Hosting of the application (artifacts / Deployable Packages ) :

 Apache Tomcat --> Web App

 ### For logs :

Apache Tomcat --> logs (Apache Tomcat and also application which is running inside Tomcat)

* We can access tomcat using local host :8080 or else 127.0.0.1:8080