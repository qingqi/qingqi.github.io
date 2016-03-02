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
The advantage of Ant lives in its flexibility to control the build process.

## Maven
Maven use *pom.xml* to configure the build process. The root element is *project*.
The build process of Maven is organized by life cycles. A life cycle define the particular steps the build process executes. Life cycles organize tasks to execute into phases, each of which consists of various tasks to execute. 3 standard life cycles are defined: clean, default/build, site. And plugins are used to bind tasks to phases. For example, the Clean plugin’s clean goal (clean:clean) is bound to the clean phase in the clean lifecycle.
A big advantage of Maven over Ant is its dependency management functionality. The life cycle convention run at cost of flexibility.

## Gradle
gradle builds around project (DAG of tasks) & task

A Gradle build has three distinct phases.

Initialization
Gradle supports single and multi-project builds. During the initialization phase, Gradle determines which projects are going to take part in the build, and creates a Project instance for each of these projects.

Configuration
During this phase the project objects are configured. The build scripts of all projects which are part of the build are executed.

Execution
Gradle determines the subset of the tasks, created and configured during the configuration phase, to be executed. The subset is determined by the task name arguments passed to the gradle command and the current directory. Gradle then executes each of the selected tasks.

plugin: conceptually import task to build script
convention is good and so is flexibility
