# Spring MVC Quickstart Maven Archetype

A Maven archetype for a simple Spring MVC web application using the following components:

* [Spring MVC](https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html) - Web Framework
* [Thymeleaf](http://www.thymeleaf.org/) - Template Engine
* [Spring Data JPA](https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html) - Data Access Layer
* [Hibernate](http://hibernate.org/) - ORM
* [SLF4J](https://www.slf4j.org/) - Simple Logging Facade for Java
* [HikariCP](https://github.com/brettwooldridge/HikariCP) - High Performance JDBC connection pool
* Other helpful utilities (Validation, DI, JSON, etc)

## Table of Contents

* [Prerequisites](#prerequisites)
* [Creating a project](#creating-a-project)
* [Testing a project](#testing-a-project)

## Prerequisites

* [Java JDK 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
* [Maven 3](https://maven.apache.org)

## Creating a Project

To start working on your new project, you will need to:

Install this archetype in your local maven repo:

```shell
git clone https://github.com/rafaelspinto/maven-archetype-spring-mvc-quickstart
cd maven-archetype-spring-mvc-quickstart
mvn clean install
```

Generate your project based on the installed archetype:

```shell
mvn archetype:generate \
        -DarchetypeGroupId=com.rafaelspinto \
        -DarchetypeArtifactId=maven-archetype-spring-mvc-quickstart \
        -DarchetypeVersion=5.0.0 \
        -DgroupId=<GROUP_ID> \
        -DartifactId=<ARTIFACT_ID> \
        -Dversion="1.0-SNAPSHOT" \
        -DinteractiveMode=false \
        -DarchetypeRepository=https://github.com/rafaelspinto/maven-archetype-spring-mvc-quickstart
```

**Note:**
Replace GROUP_ID and ARTIFACT_ID with your own.
    
## Testing a Project

If you don't want to be deploying your war file everytime you make a change, simply run the following command on the root of the project:

```shell
mvn test tomcat7:run
```


