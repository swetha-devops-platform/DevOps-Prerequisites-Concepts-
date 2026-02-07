What is Maven Architecture : 

      Maven Architecture defines how Maven builds, manages dependencies, and packages a Java project using a structured workflow and repositories.

Core Components of Maven Architecture: 

1. POM.xml (Project Object Model) – Heart of Maven

                 Configuration file for the project

                 Contains:

                     Project details (groupId(Company or organization ), artifactId (Project Name), version(Application Version) )

                     Dependencies

                     Plugins

                     Build lifecycle

Maven reads only pom.xml to execute everything


2. Maven Lifecycle

      Maven has 3 lifecycles


<img width="671" height="461" alt="Maven-Build-Life-Cycle" src="https://github.com/user-attachments/assets/21cfdcdd-46dd-42ac-8fd1-6dbc976f20e6" />


    1. Clean
   
      clean → deletes old build files
   
    2. Default (Main)
   
        validate -  validate the project is correct and information is avialable.
   
        compile  -  complie the source code

        test	  -  unit test will be happen and these test should not required the code to be packaged or delopyed
   
        package  -  packaged it in its distributabe format such as JAR
   
        Verify   -  run any checks on intergration test results to ensure quality criteria are met
   
        install  -  install package into local repository, for use as a dependency in other projects locally.
   
        deploy	  -  done in build environment, cpies the final package to remote repsitory for sharing with other developers and projects
   
   
    3. Site
   
     Generates project documentation


3. Maven Plugins

            Plugins perform actual work (compile, test, package)

            Each phase is mapped to a plugin goal

            Examples:

                       maven-compiler-plugin → compiles code

                       maven-surefire-plugin → runs tests

                       maven-jar-plugin → creates JAR


4. Repositories (Dependency Management)

            Where Libraies came from
   
      Types of Repositories:
   
              Repository	       Purpose
   
               Local	            .m2 folder on your system
   
               Central	             Default public Maven repo

               Remote	             Company/private repositories (Nexus, Artifactory)
   
     Dependency Flow:
   
                     Local → Central → Remote

If dependency not found locally, Maven downloads it and stores it locally.

5. Build Tool Engine

             Reads pom.xml

             Resolves dependencies

             Executes lifecycle phases

             Uses plugins to generate output (JAR/WAR)

Maven Architecture Flow (End-to-End)

                       Developer
                       
                          ↓
                          
                        pom.xml
                        
                          ↓
                          
                  Maven CLI (mvn install)
                  
                          ↓
                          
                  Build Lifecycle
                  
                          ↓
                          
                  Plugins Execution
                  
                          ↓
                          
                Dependency Resolution
                
                          ↓
                          
                   Repositories
                   
                          ↓
                          
                Target Folder (JAR/WAR)


Simple flow:

              You run mvn command
                     ↓
              Maven reads pom.xml
                     ↓
              Downloads libraries
                     ↓
              Builds application
