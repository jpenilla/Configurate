# Configurate
Configurate is a simple confiuration library released under the [Apache 2.0](LICENSE) that provides a node-tree representation of configurations in a variety of formats.

*Build Status*: [![Travis CI](https://travis-ci.org/zml2008/configurate.svg)](https://travis-ci.org/zml2008/configurate)


## Building
We use Maven, so this part is pretty easy. 

Configurate requires JDK 7 to build but is at runtime compatible with JDK 6 and above.

Make sure Maven is installed and from the project's directory (the root of this repository), run `mvn clean install` to build Configuate and install its artifacts to the local Maven repository.

## Usage
```xml
<dependency>
    <groupId>ninja.leaping.configurate</groupId>
    <artifactId>configurate-yaml</artifactId>
    <version>1.0</version> <!-- Update this with the most recent version -->
</dependency>
```
This dependency statement is for the yaml format implementation. Other formats managed in this repository use the same group id and versioning.
The only dependency Configurate has is on Guava (check the pom for info on which version is currently being used)

Now, to load:
```java
ConfigurationLoader loader = new YAMLConfigurationLoader(file); // Create the loader
ConfigurationNode node = loader.load(); // Load the configuration into memory

node.getNode("some", "value").getValue(); // Get the value
```
More detailed explanations of all the methods available in ConfigurationNode are available in the javadocs

## Contributing
We love PRs! However, when contributing, here are some things to keep in mind:

- In general, we follow the Oracle style guidelines for code style
- Please, please, please test PRs. It makes the process a lot easier for everybody

