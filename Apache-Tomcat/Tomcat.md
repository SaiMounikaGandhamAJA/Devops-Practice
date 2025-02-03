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

Folder Structure in Tomcat :
bin (Binary- Start and stop the server)
conf (Configuration)
lib (Library)
logs
temp (Temporary)
WebApps (To Host our Application)
Work
How to access the application :
url of tomcat>/Artifact-name

Eg : 127.0.0.1:8080/hello-world --> After pasting the artifact in webapps

mvn archetype:generate -DgroupID=com.example.aja -DartifactID=aja -DarchetypeArtifactID=maven-archetype-webapp -DinteractiveMode=false
How we can place the artifact from the maven project of target folder to apache tomcat's webapps folder ?
cp path where artifact > Path where web apps of tomcat >

(or)

cp source> destination>

(or)

destination > cp / source>

Whenever we do any configuration changes , we need to restart the server .

To change the port number of the tomcat , we need to stop the server then change the default port number to other , then you can start .

To stop the server , we have many ways

Close the terminal
Ctrl + C or Ctrl + x when you are in terminal .
To deploy the application by using GUI ?
GUI - Graphical User Interface

Access the URL of the tomcat then search for war file to deply .
Click on choose file button once we click on choose , it will open one dailogue box .
In that dailogue box we need to select the artifact and then click on WAR File .
How can we access the tomcat GUI ?
First , we need to go to the apache tomcat home folder then

home folder of apache tomcat --> conf . --> modify "tomcat-user.xml" (Using text editor)

go to below line

user username="admin"> need to uncomment those lines by removing "<!-- & --"

To view the last n no. of lines in a file .

Syntax : tail -n file-name

Example : tail -15 mouni.txt

To view the first n no. of lines in a file .
Syntax : head -n file-name

Example : head -15 mouni.txt

