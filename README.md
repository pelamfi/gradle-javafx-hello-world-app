# gradle-javafx-hello-world-app

An example of how to set up Java 15, JavaFX and Gradle application
without using the JavaFX plugin.

## Features:

  * Opens a JavaFX window with the title "Hello World!"
  * Able to run with from command line

## Gradle Commands
run in place:

    ./gradlew run 

Build a distribution zip in `build/distributions`:

    ./gradlew distZip

## Dependencies:
  * [Open JDK 15](https://adoptopenjdk.net/?variant=openjdk15&jvmVariant=hotspot)
  * [Gradle 6.6.1](https://gradle.org/install/)
  * JavaFX 15 (Will be downloaded by Gradle)

Btw. I heartily recommend [SDKMAN!](https://sdkman.io/) for installing and managing
the JDK and Gradle versions.


    sdk install java 15.0.0.hs-adpt
    sdk install gradle 6.6.1
