ci.maven.tools
==============

ci.maven.tools is a collection of Maven archetypes and target POMs for developing Java EE and OSGi applications targeting WebSphere Application Server Liberty within the WDT Eclipse IDE.

## Projects

There are provided two different projects to be used in Maven environments: [Maven Target POMs](#maven-target-poms), a set of convenience POMs that groups WebSphere Liberty dependencies; and [Maven archetypes](#archetypes), to create new Maven projects with recommended configurations and dependencies targeting WebSphere Liberty.

### [Maven Target POM's](/docs/target-poms.md)

Project containing convenience POMs that groups a set of WebSphere Liberty APIs/SPIs, java specifications and third-party dependencies provided by the runtime.

Following are the provided modules for this project: 

* [liberty-target](/docs/target-poms.md#liberty-target) - Creates a POM that provides references to all modules (APIs/SPIs, java specifications and third-party implementations).
* [liberty-apis](/docs/target-poms.md#liberty-apis) -  Creates a POM with Liberty API dependencies.
* [liberty-spis](/docs/target-poms.md#liberty-spis) -  Creates a POM with Liberty SPI dependencies.
* [java-specs](/docs/target-poms.md#java-specs) - Creates a POM with Java specification dependencies that a Liberty installation provides in the `dev/api/spec` and `/dev/spi/spec` folders.
* [third-party](/docs/target-poms.md#third-party) - Creates a POM with third-party dependencies that a Liberty installation provides in the `dev/api/third-party` and `/dev/spi/third-party` folders.
	  
### [Archetypes](/docs/archetypes.md)

Project with Maven archetypes for creating new Java EE and OSGi projects targeting WebSphere Liberty within the WDT Eclipse IDE.

#### Java EE archetypes

Archetype				| Project type
----------------------- | ------------
ejb-jee5-liberty		| EJB 3.0 project
ejb-jee6-liberty 		| EJB 3.1 project
ejb-jee7-liberty 		| EJB 3.2 project
webapp-jee5-liberty 	| Web 2.5 project
webapp-jee6-liberty 	| Web 3.0 project
webapp-jee7-liberty 	| Web 3.1 project

#### OSGi Enterprise archetypes

Archetype				| Project type
----------------------- | ------------
osgi-liberty			| OSGi project
osgi-web25-liberty		| OSGi Web 2.5 project
osgi-web30-liberty		| OSGi Web 3.0 project
osgi-web31-liberty		| OSGi Web 3.1 project

##How to build

To build and install the whole project in your local Maven repository, locate in the root folder and then execute one of the following commands in a Maven terminal.

* `mvn install`: installs the archetypes and target POMs into your local Maven repository.
* `mvn install -DskipTests`: installs the archetypes and target POMs into your local Maven repository without executing testing. 

Notice: 

* Require of Apache Maven 2.x or later.
* There's an Apache Maven issue related to archetype testing in Maven 3.3.x versions. You can workaround this, by creating a copy of "mvn.cmd" named "mvn.bat" in MAVEN_HOME/bin. For more details, see: https://issues.apache.org/jira/browse/ARCHETYPE-488
