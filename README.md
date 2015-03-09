ci.maven.tools
==============

Collection of Maven archetypes and target pom's for developing Java EE and OSGi applications targetting the  WebSphere Application Server Liberty Profile within the WDT Eclipse IDE.

## Maven Target Pom's

### liberty-target

#### Usage:  Add the following dependency to your application pom.xml to represent the Liberty and spec API libraries

	<dependency>
	  	<groupId>net.wasdev.maven.tools</groupId>
		<artifactId>liberty-target</artifactId>
		<version>LATEST</version>
	  	<type>pom</type>
	  	<scope>provided</scope>
	  </dependency>
	  
### liberty-target-impl

#### Usage:  Add the following dependency to your application pom.xml to represent the Liberty 3rd Party implementation API libraries

	<dependency>
	  	<groupId>net.wasdev.maven.tools</groupId>
		<artifactId>liberty-target-impl</artifactId>
		<version>LATEST</version>
	  	<type>pom</type>
	  	<scope>provided</scope>
	  </dependency>
	  
## Archetypes

### liberty-ejb31-archetype   - Creates EJB 3.1 Module Project targeting Liberty profile
### liberty-ejb32-archetype   - Creates EJB 3.2 Module Project targeting Liberty profile
### liberty-osgi-ejb30-archetype   - Creates OSGi with EJB 3.0 Bundle Project targeting Liberty profile
### liberty-osgi-ejb31-archetype   - Creates OSGi with EJB 3.1 Bundle Project targeting Liberty profile
### liberty-osgi-web30-archetype   - Creates OSGi with Servlet 3.0 Web Application Bundle Project targeting Liberty profile
### liberty-osgi-web31-archetype   - Creates OSGi with Servlet 3.1 Web Application Bundle Project targeting Liberty profile
### liberty-web30-archetype   - Creates Servlet 3.0 Web Application Module Project targeting Liberty profile
### liberty-web31-archetype   - Creates Servlet 3.1 Web Application Module Project targeting Liberty profile

