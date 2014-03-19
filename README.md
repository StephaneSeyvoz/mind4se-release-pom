mind4se-release-pom
===================

Maven pom project to build a full mind4se release package

# Global prerequisites

* Maven 3.0.5
* https://github.com/geoffroyjabouley/mind4se-release-scripts
* https://github.com/geoffroyjabouley/mind4se-release-manifest

# Local build

1. `mvn clean install -f ./mind-compiler/pom.xml --projects org.ow2.mind:mind-compiler`
2. `mvn clean install`

# Continuous integration

## Prerequisites

* Correct settings.xml file available into Teamforge (=S= internal)

## Build

1. `mvn -s path/to/settings.xml clean install -f ./mind-compiler/pom.xml --projects org.ow2.mind:mind-compiler`
2. `mvn -s path/to/settings.xml clean install`
3. `mvn -s path/to/settings.xml deploy -rf com.se.mind:mind4se-compiler -Dartifactory -Dteamforge`
