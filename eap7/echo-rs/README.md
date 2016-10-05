echo-rs: Echo microservice Using JAX-RS (Java API for RESTful Web Services)
==========================================================================
Author: Giuseppe Bonocore
Level: Basic__
Technologies: CDI, JAX-RS    
Summary: The `echo-rs` demonstrates a simple Echo application, bundled and deployed as a WAR, that uses *JAX-RS* to say Echo the payload.    
Target Product: JBoss EAP  
Source: 

What is it?
-----------

The `echo-rs` quickstart demonstrates the use of *CDI* and *JAX-RS* in Red Hat JBoss Enterprise Application Platform.


System requirements
-------------------

The application this project produces is designed to be run on Red Hat JBoss Enterprise Application Platform 7 or later. 

All you need to build this project is Java 8.0 (Java SDK 1.8) or later and Maven 3.1.1 or later.

Start the JBoss EAP Server
-------------------------

1. Open a command prompt and navigate to the root of the JBoss EAP directory.
2. The following shows the command line to start the server:

        For Linux:   EAP7_HOME/bin/standalone.sh
        For Windows: EAP7_HOME\bin\standalone.bat

 
Build and Deploy the Quickstart
-------------------------

1. Make sure you have started the JBoss EAP server as described above.
2. Open a command prompt and navigate to the root directory of this quickstart.
3. Type this command to build and deploy the archive:

        mvn clean install wildfly:deploy

4. This will deploy `target/jboss-helloworld-rs.war` to the running instance of the server.


Access the application 
---------------------

The application is deployed to <http://localhost:8080/echo-rs/>.

The *XML* content can be viewed by accessing the following URL (replace payload with the value you want to be echoed): <http://localhost:8080/echo-rs/xml/payload> 

The *JSON* content can be viewed by accessing this URL (replace payload with the value you want to be echoed): <http://localhost:8080/echo-rs/json/payload>


Undeploy the Archive
--------------------

1. Make sure you have started the JBoss EAP server as described above.
2. Open a command prompt and navigate to the root directory of this quickstart.
3. When you are finished testing, type this command to undeploy the archive:

        mvn wildfly:undeploy

<!-- Build and Deploy the Quickstart to OpenShift - Coming soon! -->