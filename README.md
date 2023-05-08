# Vaadin Karaf Test Project

The features module contains the test feature.

The karaf module builds a karaf archive with the test feature installable.

## Build

The Base Starter Flow OSGi Project has to be built from the V14 branch.

https://github.com/vaadin/base-starter-flow-osgi/tree/v14

First you need to build the features project

`mvn -f features/pom.xml install`

then karaf

`mvn -f karaf/pom.xml install`


## Run

Inside the karaf target folder you have the karaf archive. Alternatively you can use the target/assembly folder as well that contains the unarchived karaf.

inside the unpacked karaf folder you can start karaf with

`bin/karaf`

Once karaf is running you can install the test feature

`feature:install test`

You can now access the page via http://localhost:8080/ (Or rather not access)

You can access the webconsole via http://localhost:8080/system/console/bundles (username: karaf password: karaf)

And the log via http://localhost:8080/system/console/logs

