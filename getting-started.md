+++
title = "Getting started"
url = "gxp/getting-started.html"

[menu.gxp]
name = "Getting Started" 
+++

This tutorial describes how to get started using the Gradle xcode plugin.


### Requirements:

* Xcode 7.0 or higher
* Java 1.6 or higher
* Gradle 2.14 or higher ([see Installing Gradle](https://docs.gradle.org/current/userguide/installation.html))


## Step by Step Tutorial

Start Xcode and create a new project by selecting "Create a new Xcode Project" or by selecting the menu File -> New -> Project

![Step-01](/images/gxp/getting-started-01.png)

Select a template that you like, e.g. Single View Application

![Step-02](/images/gxp/getting-started-02.png)

Name the new Project 'Example'

![Step-03](/images/gxp/getting-started-03.png)

Save the project to a location you like e.g. 'Desktop/Demo'

![Step-04](/images/gxp/getting-started-04.png)

### Create the config file for building with gradle

Create a new empty file with New -> File -> Other -> Empty

![Step-05](/images/gxp/getting-started-05.png)

Name it 'build.gradle'

Enter the code:

```
plugins {
	id "org.openbakery.xcode-plugin" version "0.14.+"
}

xcodebuild {
	target = 'Example'
}
```

![Step-06](/images/gxp/getting-started-06.png)

### Building the App

Open the Terminal.app and navigate into the project directory (e.g. `cd ~/tmp/Demo/Example`)


Enter 'gradle xcodebuild' and the projects builds

![Step-07](/images/gxp/getting-started-07.png)

### Build Successful, so we are done

