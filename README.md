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
  * [Gradle 5.4.1](https://gradle.org/install/)
  * JavaFX 12 (Will be downloaded by Gradle)

Btw. I heartily recommend [SDKMAN!](https://sdkman.io/) for installing and managing
the JDK and Gradle versions.

    sdk install java 12.0.1-open
    sdk install gradle 5.4.1

## Background
I had some trouble setting up this example project. This branch represents an
earlier approach that does not use the plugin 'org.openjfx.javafxplugin'.

For some reason I didn't get the plugin working at first.
The [master branch in my example repository](https://github.com/pelamfi/gradle-javafx-hello-world-app) now uses the plugin.

However, I still feel that perhaps a plugin like this should not be necessary
for a simple case and there should be a way to cleanly configure `--module-path`
and the `--add-modules` settings. Due to this 
[I filed a bug in the Gradle project](https://github.com/gradle/gradle/issues/9309) using
this branch as an example. Perhaps I'll just learn something more and can then improve
these examples.
