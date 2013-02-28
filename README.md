Pomade
======

Pomade is a Maven parent pom offering à la carte selection of common dependency 
groups and build profiles.  Use Pomade as the parent of your next Maven 
project and start coding faster!

Features
--------

* Select from predefined dependency collections for commonly used Java libraries:
    * [SLF4J](http://www.slf4j.org/) with [Logback](http://logback.qos.ch/) 
    * [Hibernate](http://www.hibernate.org/) with [Ehcache](http://ehcache.org/) and [c3p0](https://github.com/swaldman/c3p0)
    * Favorite [Apache Commons](http://commons.apache.org/) projects
* Measure and enforce minimum unit test coverage with [Jacoco](http://www.eclemma.org/jacoco/).
* Execute JUnit tests in [parallel](http://maven.apache.org/surefire/maven-surefire-plugin/examples/junit.html#Running_tests_in_parallel).
* Build -sources.jar and -javadoc.jar artifacts during the package phase of your build.
* Sign artifacts during the verify phase of your build.
* Enforce Maven best practices like explicit plugin versions, specific Java version, etc.

Quick Start
-----------

Declare Pomade as your parent pom:
```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
    <modelVersion>4.0.0</modelVersion>
    
    <!-- inherit from Pomade -->
    <parent>
        <groupId>net.big-oh</groupId>
        <artifactId>pomade</artifactId>
        <version>1.0-SNAPSHOT</version>
    </parent>
    
    <!-- describe your project -->
    <groupId>foo.bar</groupId>
    <artifactId>baz</artifactId>
    <version>1.0-SNAPSHOT</version>
</project>
```

Select one or more dependency groups to be used by your project:
```bash
$ mkdir src/pomade
$ touch src/pomade/use.slf4j
$ touch src/pomade/use.hibernate
$ touch src/pomade/use.h2
$ touch src/pomade/use.commons
```