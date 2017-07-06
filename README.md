# GeoSpark Template Project
[![Build Status](https://travis-ci.org/jiayuasu/GeoSparkTemplateProject.svg?branch=master)](https://travis-ci.org/jiayuasu/GeoSparkTemplateProject)

This repository contains four template projects for GeoSpark and Babylon (v0.1.X-0.2.X). The template projects have been configured properly. You are able to compile, package, and run the code locally without any extra coding.

GeoSpark repository is available here: [GeoSpark GitHub Repository](https://github.com/DataSystemsLab/GeoSpark)

## Folder structure
The folder structure of this repository is as follows.

* geospark
  * scala: **GeoSpark Scala Template Project**
  * java: **GeoSpark Java Template Project**
* babylon (v0.1.X-0.2.X)
  * scala: **Babylon (v0.1.X-0.2.X) Scala Template Project**
  * java: **Babylon (v0.1.X-0.2.X) Java Template Project**

## Compile and package

### Prerequisites
Please make sure you have the following software installed on your local machine:

* For Scala: Scala 2.11, SBT
* For Java: JDK 1.8, Apache Maven 3

### Git Clone
```
$ git clone https://github.com/jiayuasu/GeoSparkTemplateProject.git
```

### GeoSpark Scala Template Project

```
$ cd ./geospark/scala
$ sbt assembly
```

### GeoSpark Java Template Project

```
$ cd ./geospark/java
$ mvn clean install
```

### Babylon Scala Template Project

```
$ cd ./babylon/scala
$ sbt assembly
```
### Babylon Java Template Project

```
$ cd ./babylon/java
$ mvn clean install
```
### Submit your fat jar to Spark
After running the command mentioned above, you are able to see a fat jar in `./target` folder. Please take it and use `./bin/spark-submit` to submit this jar.

Note: you need to change Spark Master Address in template projects if you want to run the jar in your Spark cluster. Currently, they are hard coded to `local[4]` which means run locally with 4 cores.

## Run template projects locally
We highly suggest you use IDEs to run template projects on your local machine. For Scala, we recommend IntelliJ IDEA with Scala plug-in. For Java, we recommend IntelliJ IDEA and Eclipse. With the help of IDEs, **you don't have to prepare anything** (even don't need to download and set up Spark!). As long as you have Scala and Java, everything works properly!

### Scala
Import the Scala template project as SBT project. Then run the Main file in this project.

### Java
Import the Java template project as Maven project. Then run the Main file in this project.

### Note
* After running your Babylon template project, you should be able to see a folder at `./target/demo`. This folder contains all the raster/vector images generated by Babylon using test data.

* For IntelliJ IDEA users, you probably have to click "File->Project Structure->Global Libraries-> + >From Maven..." to add Spark-core, GeoSpark and Babylon Maven Dependencies in order to run projects in the IDE.
