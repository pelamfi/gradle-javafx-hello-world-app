# gradle-javafx-hello-world-app

An example of how to set up Java 14, JavaFX 14 and Gradle application.

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
  * [Open JDK 14](https://adoptopenjdk.net/?variant=openjdk14&jvmVariant=hotspot)
  * [Gradle 6.3](https://gradle.org/install/)
  * JavaFX 14 (Will be downloaded by Gradle)

Btw. I heartily recommend [SDKMAN!](https://sdkman.io/) for installing and managing
the JDK and Gradle versions.


    sdk install java 14.0.0.hs-adpt
    sdk install gradle 6.3

## Background
I had some trouble setting this example up, but it turns out that the 
[org.openjfx.javafxplugin Gradle plugin](https://github.com/openjfx/javafx-gradle-plugin)
works great.

I also have an 
[earlier branch of this example](https://github.com/pelamfi/gradle-javafx-hello-world-app/tree/gradle-javafx-run-working-without-plugin-and-with-hacks) 
that reaches the same goals without using the JavaFX Gradle
plugin, but that seems to require some strange hacks that the plugin probably takes care of.
