java8-quickstart-archetype
==========================

A bloody simple Java 8 archetype. Has the following features:

 * minimizes the amount of "example" files that you would have to delete anyway (cf. `maven-quickstart-archetype`).
 * automatically creates *empty* package directories for `main` and `test`.
 * let's you setup many Java 8 configuration variants for all your legacy needs (see `Usage`).
 * optionally includes JUnit or TestNG dependencies (JUnit by default).
 
In general, this archetype is primarily useful for quickly creating "lite" projects that are intended to run on a Java 8 JRE.

Usage
=====

Analogous to `maven-quickstart-archetype`. Until the artifact ends up in Maven Central, you can use it as follows:

```bash
git clone https://github.com/mikkoz/java8-quickstart-archetype.git
cd java8-quickstart-archetype
mvn clean install
cd x #where x is your "workspace" directory
mvn archetype:generate
#filter by e.g. "java8"
#input artifactId etc. 
```

And here's an infodump from the project's description:

Basic Java 8 archetype. Options:

* `testLibrary`: [`junit`, `testng`, `none`]. DEFAULT: `junit`. Adds the requested test library to the POM deps.
* `compilerMode`: [`simple`, `test-only`, `retrolambda-main`, `retrolambda-all`]. DEFAULT: `simple`.
 * `simple`: everything is compiled as Java 8.
 * `test-only`: set up test for Java 8, and main for Java 7.
 * `retrolambda-main`: main code is compiled as Java 8, and then converted to Java 7 via retrolambda.
 * `retrolambda-all`: all code is compiled as Java 8, and then converted to Java 7 via retrolambda.

NOTE: Retrolambda support provided "as is" - if you have any problems, please file a ticket on the GitHub page!

Why yet another archetype?
=========================

The sister-project Scala archetype cointains a [ranty explanation for that](https://github.com/mikkoz/scala-quickstart-archetype/blob/master/README.md#why-yet-another-archetype).