---
id: setup-building
title: Setup and Building
sidebar_label: "Setup and Building"
---

## Prerequisites

| Dependency | Description                                                                                                                                                                                                      |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Git        | The source code of Pulsar is hosted on GitHub as a git repository. To work with the git repository, please [install git](https://git-scm.com/downloads).                                                         |
| JDK        | The source code of Pulsar is almost written in Java. Therefore, you need a working Java Development Kit (JDK) to build it. Pulsar requires [JDK 17](https://adoptium.net/temurin/releases/?version=17) to build. |
| Maven      | The source code of Pulsar is managed by [Apache Maven](https://maven.apache.org/) The required Maven version is 3.6.1+.                                                                                          |
| Zip        | The build process requires Zip as a utility tool.                                                                                                                                                                |

:::note

This project includes a [Maven Wrapper](https://maven.apache.org/wrapper/) that can be used instead of a system installed Maven. Use it by replacing `mvn` with `./mvnw` on Linux and `mvnw.cmd` on Windows in the commands below.

:::

## Clone

Clone the source code to your development machine:

```bash
git clone https://github.com/apache/pulsar
```

## Build

Compile and install:

```bash
mvn clean install -DskipTests
```

## Run unit tests

```bash
mvn test
```

Run individual unit test:

```bash
# mvn -pl <module-name> test -Dtest=<unit-test-name> # for example:
mvn -pl pulsar-client test -Dtest=ConsumerBuilderImplTest
```

## Start standalone Pulsar service

```bash
bin/pulsar standalone
```

## Connect to the standalone service:

```bash
bin/pulsar-shell
```
