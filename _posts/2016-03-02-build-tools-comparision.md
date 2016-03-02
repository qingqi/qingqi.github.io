---
layout: post
title: "Build Tools Comparisons: Ant, Maven, and Gradle"
excerpt: "comparison between Ant, Maven and Gradle"
modified: 2016-03-02
tags: [intro, beginner, basics, ant, maven, gradle, build tools]
comments: true
---

## Ant
Ant uses *build.xml* to configure the build process. The root element is *project*.
The fundamental concept of *build.xml* is to configure projects by graphs of targets linked by dependencies.
The advantage of Ant lives in its **flexibility** to control the build process.

## Maven
Maven use *pom.xml* to configure the build process. The root element is *project*.
The build process of Maven is organized by life cycles. A life cycle define the particular steps the build process executes. Life cycles organize tasks to execute into phases, each of which consists of various tasks to execute. 3 standard life cycles are defined: clean, default/build, site. And plugins are used to bind tasks to phases. For example, the Clean plugin’s clean goal (clean:clean) is bound to the clean phase in the clean lifecycle.
An advantage of Maven over Ant is its dependency management functionality. The life cycle **convention over configuration** run at cost of flexibility.

## Gradle
Gradle use *build.gradle* to configure the build process. Gradle builds around concepts of projects and tasks. A project is conceptually directed acyclic graph (DAG) of tasks. The edges in the DAG denotes dependency relationship.
Gradle plugin conceptually import tasks to build script. **Gradle combines the flexibility of Ant and convention over configuration of Maven**.

A Gradle build has three distinct phases: initialization, configuration, and execution. In initialization, Gradle determines which projects are going to take part in the build, and creates a Project instance for each of these projects. In Configuration, the project objects are configured. The build scripts of all projects which are part of the build are executed. In execution, Gradle determines the subset of the tasks to be executed. The subset is determined by the task name arguments passed to the gradle command and the current directory. Gradle then executes each of the selected tasks.
