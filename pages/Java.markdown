---
title: Java Notes by AlasdairMorrison.com
---

#### Reading from a properties file
Create myProp.properties in the src directory and then use the following code
```java
ResourceBundle rb= ResourceBundle.getBundle("myProp.properties");
Sting coolProperty = rb.getString(“propertyIWantToGet”)
```

#### Write using log4j
```java
import org.apache.log4j.Logger;

import java.io.*;
import java.sql.SQLException;
import java.util.*;

public class log4jExample{
  /* Get actual class name to be printed on */
  static Logger log = Logger.getLogger(
                      log4jExample.class.getName());

  public static void main(String[] args)
                throws IOException,SQLException{
   
     log.debug("Hello this is an debug message");
     log.info("Hello this is an info message");
  }
}
```

#### Ant vs Maven vs Gradle
http://technologyconversations.com/2014/06/18/build-tools/ 

#### SSH into JVM and change code!!
https://github.com/palominolabs/jvm-ssh-groovy-shell 

#### Java File Formats
In J2EE application modules are packaged as EAR, JAR and WAR based on their functionality
#### EJB Jar Files
JAR: EJB modules which contains enterprise java beans class files and EJB deployment descriptor are packaged as JAR files with .jar extension.

EJB container hosts enterprise java beans based on EJB API designed to provide extended business functionality such as declarative transactions, declarative method level security and multi protocol support - more of RPC style of distributed computing. EJB container required EJB module to be packaged in JAR file having ejb-jar.xml file in META-INF folder.
#### War Files
WAR: Web modules which contains Servlet class files,JSP FIles,supporting files, GIF and HTML files are packaged as JAR file with .war (web archive) extension.

WAR (Web Archive) is a module that goes into web container of Java EE application server. A Java EE application server has two containers (run time environments) - one is a web container and the other is a EJB container

The Web container hosts web applications based on JSP/Servlets API - designed specifically for web request handling - more of request/response distributed computing. Web container requires the web module to be packaged in WAR file that is special JAR file with web.xml file in WEB-INF folder

#### Ear Files
EAR: All above files (.jar and .war) are packaged as JAR file with .ear (enterprise archive) extension and deployed into Application Server.

Enterprise application may consist of one or more than modules that can either be Web modules (packaged in WAR file) or EJB modules (packaged in JAR file) or both of them. Enterprise applications are packaged in EAR file that is special JAR file containing application.xml file in META-INF folder

Basically EAR file is superset containing WAR file and JAR files. Java EE application servers allow deployment of standalone web modules in WAR file though internally they create EAR file as wrapper around WAR files. 
Tomcat doesn’t support Ear
Standalone web container such as tomcat and jetty do not support EAR files - these are not full fledged application servers. Web applications in these containers are to be deployed as WAR file only.

#### Maven
Maven is a build tool which handles dependencies, can be used to both build and deploy java applications.

#### Apache Tomcat
This is a very easy to use appserver for java web applications.

catalina start

#### RestX Lightweight Java Server
Very lightweight java server:
http://restx.io/docs/install.html

### Java Design Patterns

#### Inversion of Control (Strategy Pattern)

http://architects.dzone.com/articles/unit-testing-101-inversion 

