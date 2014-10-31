ci.maven.tools
==============

Collection of Maven archetypes and target pom's for developing Java EE and OSGi applications targetting the  WebSphere Application Server Liberty Profile within the WDT Eclipse IDE.

## Maven Target Pom's

### liberty-target

#### Usage:  Add the following dependency to your application pom.xml to represent the Liberty classpath

<dependency>
  	<groupId>net.wasdev.maven.tools</groupId>
	<artifactId>liberty-target</artifactId>
	<version>8.5.5.4</version>
  	<type>pom</type>
  	<scope>provided</scope>
  </dependency>