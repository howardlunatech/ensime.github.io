---
layout: section
order: 4
title: Maven
---

This maven plugin generates a `.ensime` file and provides various convenience commands for interacting with [ENSIME](http://github.com/ensime/ensime-server). The source code can be found at in it's own project: [ensime-maven](https://github.com/ensime/ensime-maven/).

# ENSIME Maven Plugin

This [maven](https://maven.apache.org/) plugin generates a `.ensime` file for use with an [ENSIME server](http://github.com/ensime/ensime-server).

## Installation

Configure your `~/.m2/settings.xml` file so that maven is aware of the plugin group `org.ensime.maven.plugins`:

```xml
  <pluginGroups>
    <pluginGroup>org.ensime.maven.plugins</pluginGroup>
  </pluginGroups>
```

Then add the following to your `pom` file:

```xml
<plugin>
  <groupId>org.ensime.maven.plugins</groupId>
  <artifactId>ensime-maven</artifactId>
  <version>0.0.6</version>
</plugin>
```

## Generate `.ensime` file

To actually generate the `.ensime` file from your pom, run:

```
mvn ensime:generate
```
