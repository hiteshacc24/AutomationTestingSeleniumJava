# Automation Testing using Selenium, Java, Maven, TestNG
The path from a Quality Tester to Quality Engineer

For this series, I will be using Selenium with the Java programming language and the TestNG library, which will make our efforts easier and more organized. My IDE of choice is IntelliJ Idea.

###Prerequisites:

1. Working Knowledge of Java
2. Working Knowledge of Maven

Make sure you have installed on your machine: a Java Development Kit (JDK 1.8 preferably), Maven, and IntelliJ Idea.

### Setup and Installations

Download the community edition of IntelliJ Idea

[Idea](https://www.jetbrains.com/idea/download/#section=mac)

[JDK](https://www.oracle.com/java/technologies/javase-downloads.html)

Maven should be installed with IntelliJ Idea

In brief, and for those using IntelliJ Idea: the simplest way to get started is to start a new project and, in the New Project window, choose Maven, check the Create from archetype box, and then Next. Fill in your chosen GroupId and ArtifactId, then hit Next to complete the process.

You should then see your new pom.xml file. This, for those unfamiliar with Maven, contains all your project’s dependencies, settings, and much more. We then have to add the Selenium and TestNG dependencies, just like in the example below.


```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>org.example</groupId>
    <artifactId>TestMavenProject</artifactId>
    <version>1.0-SNAPSHOT</version>
    <properties>
        <maven.compiler.source>1.10</maven.compiler.source>
        <maven.compiler.target>1.10</maven.compiler.target>
    </properties>
    <dependencies>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>4.13</version>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>3.141.59</version>
        </dependency>
        <dependency>
            <groupId>org.testng</groupId>
            <artifactId>testng</artifactId>
            <version>7.1.0</version>
            <scope>test</scope>
        </dependency>
        <!-- https://mvnrepository.com/artifact/com.aventstack/extentreports -->
        <dependency>
            <groupId>com.aventstack</groupId>
            <artifactId>extentreports</artifactId>
            <version>3.0.0</version>
        </dependency>
        <dependency>
            <groupId>com.relevantcodes</groupId>
            <artifactId>extentreports</artifactId>
            <version>2.41.1</version>
        </dependency>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>RELEASE</version>
            <scope>test</scope>
        </dependency>
    </dependencies>
</project>
```



