java8-quickstart-archetype
==========================

A bloody simple Java 8 archetype. Has the following features:

 * minimizes the amount of "example" files that you would have to delete anyway (cf. `maven-quickstart-archetype`).
 * automatically creates *empty* package directories for `main` and `test`.
 * currently includes an up-to-date JUnit dependency. Up for reconsideration.
 
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