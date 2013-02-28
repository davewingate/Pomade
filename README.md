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
* Sign your artifacts during the verify phase of your build.
* Enforce Maven best practices like explicit plugin versions, specific Java version, etc.