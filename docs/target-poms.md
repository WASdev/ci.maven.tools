Maven target POMs
=================

This project contains all convenience POMs that list WebSphere Liberty dependencies aligned to the latest release of Liberty to develop Java EE and OSGi applications.

Dependencies are grouped in following modules:

* liberty-target - All WebSphere Liberty dependencies (APIs/SPIs, java specifications and third-party implementations)
* liberty-apis -  WebSphere Liberty APIs dependencies
* liberty-spis - WebSphere Liberty SPIs dependencies
* java-specs - Java specifications dependencies
* third-party - Third-party implementations

## Project structure

	targets/ - Parent to build all modules
		pom.xml
		java-specs/	- Java specifications module
			pom.xml
		liberty-apis/ - WebSphere Liberty APIs module
			pom.xml
		liberty-spis/ - WebSphere Liberty SPIs module
			pom.xml
		liberty-target/ - Aggregator of all modules
			pom.xml
		third-party/ - Third-party dependencies module
			pom.xml

##Usage information

Following modules add WebSphere Liberty dependencies to your project. Add the dependency snippet to your Maven project to reference all dependencies automatically.

It's important to notice that the version of the `liberty-target`, `liberty-apis` and `liberty-spis` are aligned to the release of WebSphere Liberty, so you can use older versions by changing the version of those artifacts.

###liberty-target

This project aggregates all other modules that references WebSphere Liberty APIs/SPIs, java specifications and third-party implementations dependencies to compile your project.

Dependency snippet:

	<dependency>
		<groupId>net.wasdev.maven.tools.targets</groupId>
		<artifactId>liberty-target</artifactId>
		<version>RELEASE</version>
		<type>pom</type>
		<scope>provided</scope>
	</dependency>
	
###liberty-apis

WebSphere Liberty API's dependencies. This POM satisfies all APIs libraries that a Liberty installation provides in the `dev/api/ibm` folder.

Dependency snippet:

	<dependency>
		<groupId>net.wasdev.maven.tools.targets</groupId>
		<artifactId>liberty-apis</artifactId>
		<version>RELEASE</version>
		<type>pom</type>
		<scope>provided</scope>
	</dependency>

###liberty-spis

WebSphere Liberty SPI's dependencies. This POM satisfies all SPIs libraries that a Liberty installation provides in the `dev/spi/ibm` folder.

Dependency snippet:

	<dependency>
		<groupId>net.wasdev.maven.tools.targets</groupId>
		<artifactId>liberty-spis</artifactId>
		<version>RELEASE</version>
		<type>pom</type>
		<scope>provided</scope>
	</dependency>

###java-specs

Java specification dependencies. This POM satisfies all Java specification libraries that a Liberty installation provides in the `dev/api/spec` and `dev/spi/spec` folders.

Dependency snippet:

	<dependency>
		<groupId>net.wasdev.maven.tools.targets</groupId>
		<artifactId>java-specs</artifactId>
		<version>RELEASE</version>
		<type>pom</type>
		<scope>provided</scope>
	</dependency>


###third-party

Third-party implementation dependencies. This POM satisfies all third-party libraries that a Liberty installation provides in the `dev/api/third-party` and `dev/spi/third-party` folders.

Dependency snippet:

	<dependency>
		<groupId>net.wasdev.maven.tools.targets</groupId>
		<artifactId>third-party</artifactId>
		<version>RELEASE</version>
		<type>pom</type>
		<scope>provided</scope>
	</dependency>

##How to build

To build the whole target POMs project locate in the `targets/` folder and execute following command in a Maven terminal:

`mvn install`: builds and install all target POMs in the local repository.

If you need to build one of the modules, just locate in the module folder you want and execute the previous command.