## `Build Tool :`

### `Apache Maven :` Maven is a build automation tool which is powered by Apache foundation.

* Maven is a tool that is used to compile , validate codes and analysis the test-cases in the code .

* It Manages the building , reporting and documentation from source code management (SCM)

* Maven Projects are configured through project object model (POM)

  (or)
* Maven uses a configuration file called POM.XML (Project Object Model) where you define project dependencies,plugins and other project details.
* POM.XML file contains documentation for all of the objects , properties , methods and events 
* Maven is a platform independent and free & Open source

## `Build tools for programming languages :`

* Java : Maven , Gradle and Ant
* .net : Ms Build
* Java Script / Type Script : NPM ( Node Package Manager )
* Python : Setup tools , Py builder
* C / C++ : Make
* PHP : Composer

## key concept of Maven : 
 
 * `Project Object Model (POM):` A fundamental part of Maven is the pom.xml file.
                                     
   - It defines the configuration of the project, such as project dependencies, plugins, build profiles, and other settings. 
                          
    - This file is the heart of Maven, describing how to build and manage the project.



* `Dependencies:` These are external libraries(libraries refer to external code or components) that your project needs. 
                        
     - Maven automatically downloads and manages them for you.

     - libraries are predefined configuration code to run our project in the function correctly(optional)



* `Repositories:` Repositories store the libraries and dependencies.

    *  Maven uses local (on your computer) and remote (e.g., Maven Central) repositories to fetch and store dependencies.



* ` Build Lifecycle Phases`: A series of phases 
  - eg: Validate , Compile , Test , Package , Integration - test , Verify , Install , deploy

  - These are define the process of building, testing, and packaging the project.




* `Plugins:` Plugins are used to perform specific tasks 
      
     - eg: compiling code, running tests, packaging applications,They are configured in the pom.xml.



* `Goal:` Maven goal is an individual task that Maven executes during the build process.

  - Each goal is typically associated with a plugin such as compiling code, running tests,packaging the application.
 

##  What maven is capable (or) Advantages :
  
 1. It automatically handles and downloads necessary libraries for your project.

 2. It gives your project a consistent structure, making it easier to work with

3. It automates the steps for compiling, testing, and packaging your project.
     
 4. It easily integrate with tools like Jenkins for automated builds (or) Easily integrates with CI tools for automated builds.

5. It allows you to set up different environments (like development and production) easily.

6. Maven manages versions of dependencies and project releases.

## `Maven Build Life Cycle :`

* In Maven , the build is run using a predefined and ordered set of steps to call the build life-cycle
* The build tasks that will be performed during each phase are determined by the configuration in the project file and in particular the selected packaging.
* Maven relies on build lefecycles to define the process of building and distributing artifacts (eg: Jar files , war files)

### `Built-in Build Lifecycles :`
There are 3 built in built life cycles 

* `Default :` Manages the build and deployment process of the project.
 
* `Clean :` Handles project cleaning.
* `Site :` Generates project documentation and reports.

## `Maven Lifecycle Phases :`
 There are 8 phases in maven life cycle
  * `validate :` Check if the project is correct , having all the necessary information .
    * `Syntax:` mvn validate
* `Compile :` Compiles the source code of the project.
   * `Syntax:`  mvn compile
* `Test :`  Runs unit tests on the compiled source code using testing frameworks like JUnit.
  * `Syntax:`  mvn test
* `Package :` Packages the compiled code into a deployable format (e.g., JAR, WAR, EAR).
  *  `Syntax:`  mvn package

* `Integration test :` process and deploy the package into an environment where integration tests can be run
  * `Syntax:`  mvn integration-test
* verify: Verifies that the packaged code meets the quality criteria 
  * `Syntax:`  mvn verify

* `install:` Installs the packaged code into the local Maven repository, making it available for other projects on the same machine.
  * `Syntax:`  mvn install
* `deploy :` deploy: Deploys the packaged code to a remote repository (eg: Maven Central or a private repository) for sharing with other developers or applications.
  * `Syntax:`  mvn deploy

 ### `Maven Architecture :` 
  - Remote repository is reffering to organisation level

   - local repository is reffering to local machine (window's)

   - central repository is reffering to apache maven

### `Maven Artifact :`
  
 - Maven artifact is file such as war,jar,ear files used by a Maven project.

  - Maven artifacts are stored in repositories,so they can be used as dependencies by other projects

  - Maven artifacts are identified by three components 

       1. group ID: A unique identifier for the group or organization

      2. Artifact ID: A unique identifier for the artifact within the group. 

      3. version : also called artifact co-ordinates

## Maven Repository Flow :

  **Step 1:** When developer executes mvn command, it will go and check in local repository. If found the dependencies and plugins in the local repository, developer will get the artifact.

  **Step 2:** If not found it in local repository from developer machine, it will go and search in remote repository.

  **Step 3:** From remote repository, required dependency or plugins will get stored in local repository.

  **Step 4:** From local repository, developer will get the artifact.
 
## Project Object Model (POM):

   - Pom is short

   - XML file located at the root of the project (pom.xml)

   - It includes configuration for your project, including :

        1. Information about the project

        2. Configuration details to build the project

        3. Contains default values for most of the projects

           eg: source directory, target directory

       4. Dependencies of the project

       5. Configuration about plugins and goals

* Declaring Dependencies :
 
   - while declaring the dependencies , co-ordinates of the artifacts must be provided

    such as : group id , artifact id, version



## pre-requasites : 

   1. JDK (Java Development Kit) installed.

   2. Maven installed on your system.

   3. Set MAVEN_HOME and update the PATH environment variable.

   4. Internet access for downloading dependencies.




## What is .m2 folder ..?

   - The .m2 folder is Maven's local repository where it stores downloaded dependencies and plugins. It helps avoid re-downloading artifacts each time you build a project.
     
  - It's located in your home directory (eg : ~/.m2)

 
