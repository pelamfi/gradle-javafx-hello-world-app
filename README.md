# gradle-javafx-hello-world-app

An example of how to set up Java 12, JavaFX and Gradle application.

## Features:

  * Opens a JavaFX window with the title "Hello World!"
  * Able to build a working runnable distribution zip file (Windows to be tested)
  * Able to open and run in IntelliJ without additional configuration
  * Able to run with from command line

## Gradle Commands
run in place:

    ./gradlew run 

Build a distribution zip in `build/distributions`:

    ./gradlew distZip


## Dependencies:
  * [Open JDK 12](https://adoptopenjdk.net/?variant=openjdk12&jvmVariant=hotspot)
  * [Gradle 5.4](https://gradle.org/install/)
  * JavaFX 12 (Will be downloaded by Gradle)

Btw. I heartily recommend [SDKMAN!](https://sdkman.io/) for installing and managing
the JDK and Gradle versions.


    sdk install java 12.0.1-open
    sdk install gradle 5.4

## Background
Unfortunately it seems that various tools haven't quite moved up to speed with either
Java modules and/or JavaFX. A simple app setup like this seems way harder than it
should be. (Either that or I'm missing something obvious like a gradle plugin or
configuration. I hope this is the case and I will soon discover what it is.)

The JavaFX Gradle plugin does not seem to work, possibly with the recent versions of
 other software I'm trying to use.
This example project does not use the JavaFX plugin for now. Here is how
it would be applied according to docs:

    // Does not seem to work as documented in https://openjfx.io/openjfx-docs/#gradle
    id 'org.openjfx.javafxplugin' version '0.0.7'
    
I'm considering filing bugs to involved parties once I have some clue as
to what goes wrong.

Currently the `build.gradle` contains various workarounds
that should not be necessary.
