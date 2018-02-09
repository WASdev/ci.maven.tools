Archetypes
==========

This multi-module project contains archetypes to develop new Maven Java EE and OSGi projects with recommended configurations and dependencies targeting WebSphere Liberty.

*Note: Usage of following archetypes is recommended with WAS Developer Tools (WDT) for Eclipse IDE.*

## Project structure

	archetypes/ - Parent POM to build all archetypes
		pom.xml 
		ejb-jee5-liberty/ - EJB 3.0 archetype module
			pom.xml
		ejb-jee6-liberty/ - EJB 3.1 archetype module
			pom.xml
		ejb-jee7-liberty/ - EJB 3.2 archetype module
			pom.xml
		osgi-liberty/ - OSGI archetype module
			pom.xml
		osgi-web25-liberty/ - OSGi Web 2.5 archetype
			pom.xml
		osgi-web30-liberty/ - OSGi Web 3.0 archetype
			pom.xml
		osgi-web31-liberty/ - OSGi Web 3.1 archetype
			pom.xml
		osgi-web40-liberty/ - OSGi Web 4.0 archetype
			pom.xml
		webapp-jee5-liberty/ - Web 2.5 archetype
			pom.xml
		webapp-jee6-liberty/ - Web 3.0 archetype
			pom.xml
		webapp-jee7-liberty/ - Web 3.1 archetype
			pom.xml
		webapp-jee8-liberty/ - Web 4.0 archetype
			pom.xml

## Archetypes list

Following is the list of provided archetypes. The Archetypes groupId is `net.wasdev.maven.tools.archetypes` 

### Java EE archetypes

Archetype artifactId	| Project type
----------------------- | ------------
ejb-jee5-liberty		| EJB 3.0 project
ejb-jee6-liberty 		| EJB 3.1 project
ejb-jee7-liberty 		| EJB 3.2 project
webapp-jee5-liberty 	| Web 2.5 project
webapp-jee6-liberty 	| Web 3.0 project
webapp-jee7-liberty 	| Web 3.1 project
webapp-jee8-liberty 	| Web 4.0 project

### OSGi Enterprise archetypes

Archetype artifactId	| Project type
----------------------- | ------------
osgi-liberty			| OSGi project
osgi-web25-liberty		| OSGi Web 2.5 project
osgi-web30-liberty		| OSGi Web 3.0 project
osgi-web31-liberty		| OSGi Web 3.1 project
osgi-web40-liberty		| OSGi Web 4.0 project

## Usage information

You can use the provided archetypes by using WDT for Eclipse IDE and by CLI.

### Usage with WDT for Eclipse IDE

1. Open the New Project Wizard by selecting **File/New/Other...** menu.
2. In the Filter textbox type **Maven Project** and press **Next** button.
3. Press again **Next** button and then ensure the **All Catalogs** option is selected in the **Catalog** combo box.
4. In the **Filter** textbox type **net.wasdev.maven.tools.archetypes**.
5. Select one of the provided archetypes and then follow the Wizard.
6. Once completed, wait until all processes conclude and WDT for Eclipse IDE will install project facets and configure your Maven project in base of the archetype you chose at step 5.

### Usage by CLI

Open a Maven terminal and then execute following command to generate a new Maven project:

`mvn archetype:generate -DarchetypeArtifactId=<archetype_artifact_id> -DarchetypeGroupId=net.wasdev.maven.tools.archetypes`

After executing the command the interactive mode will be asked for some values like your artifactId, groupId and version for your project before finishing.

## How to build

*Before building this project in your machine, ensure you have installed the [target POMs project](../docs/target-poms.md) as archetypes use net.wasdev.maven.tools.targets:liberty-target:RELEASE dependency*.

To build the whole archetypes project locate in the `archetypes/` folder and execute following command in a Maven terminal:

`mvn install`: builds and install all archetypes in the local repository.

If you need to build one of the modules, just locate in the module folder you want and execute the previous command.
