+++
title = "Gradle Xcode Plugin"
cover = true
url = "/gxp"
image = "ToolsDark.jpg"
github = "http://github.com/openbakery/gradle-xcodePlugin"

[menu.main]
name = "Gradle Xcode Plugin"
identifier = "gxp"
weight = 0



+++

# About


The Gradle Xcode plugin is a plugin for the [Gradle](http://gradle.org) build management tool that adds support for building Xcode projects. The goal is to have an easy and reliable build process for iOS or macOS Applications. 
The build can be executed on the developers machine also integrate nicely various build servers like [Jenkins](http://jenkins-ci.org), [Go](http://go.cd), etc.  
The plugin not only builds the application, it also has support for code signing, packaging and distribution.
This can be all configured with a single configuration file.


# Usage

### Requirements:

* Xcode 7 or greater
* Gradle 2.14 or greater
* Java 1.6 or greater



### Usage

Create a build.gradle file and place it in the same directory where xcodeproj file lies.

Here the minimal content you need in your build.gradle file:
(Replace the MY-TARGET with your target you use in Xcode)


<pre>
<code class="groovy">
plugins {
  id "org.openbakery.xcode-plugin" version "0.14.3"
}

xcodebuild {
  target = 'MY-TARGET'
}
</code>
</pre>

Now open the Terminal.app and navigate into the project directory and run <code>gradle xcodebuild</code> and your project should compile. You find the all output in the <code>build</code> folder.

### Tutorial:

See [the getting started tutorial](getting-started.html).

### Options

For all available build task run <code>gradle tasks</code> and you get the following output:

<pre>
<code class="groovy">
------------------------------------------------------------
All tasks runnable from root project
------------------------------------------------------------

Analytics tasks
---------------
cpd - Runs the CPD report on Objective C code
oclint - Runs: clean xcodebuild oclintReport
oclintReport - Create a OCLint report for the given project

Appledoc tasks
--------------
appledoc - Runs the appledoc for the given project
appledocClean - Cleans up the generated files from appledoc

AppStore tasks
--------------
appstoreUpload - Distributes the build to Apples Appstore
appstoreValidate - Validates the created ipa

Build tasks
-----------
assemble - Assembles the outputs of this project.
build - Assembles and tests this project.
clean - Deletes the build directory.

Build Setup tasks
-----------------
init - Initializes a new Gradle build. [incubating]
wrapper - Generates Gradle wrapper files. [incubating]

Carthage tasks
--------------
carthageClean - Cleans up the Carthage directory
carthageUpdate - Installs the carthage dependencies for the given project

Cocoapods tasks
---------------
cocoapodsBootstrap - Bootstraps cocoapods
cocoapodsInstall - Installs the pods for the given project
cocoapodsUpdate - Updates the pods for the given project

Coverage tasks
--------------
coverage - Runs the gcovr code coverage for the project
coverageClean - Cleans up the generated files from the coverage

Crashlytics tasks
-----------------
crashlytics - Upload the IPA to crashlytics for crash reports

DeployGate tasks
----------------
deploygate - Distributes the build to DeployGate
deploygateClean - Cleans up the generated files from the deploygate target

Help tasks
----------
buildEnvironment - Displays all buildscript dependencies declared in root project 'OBTableViewController'.
components - Displays the components produced by root project 'OBTableViewController'. [incubating]
dependencies - Displays all dependencies declared in root project 'OBTableViewController'.
dependencyInsight - Displays the insight into a specific dependency in root project 'OBTableViewController'.
help - Displays a help message.
model - Displays the configuration model of root project 'OBTableViewController'. [incubating]
projects - Displays the sub-projects of root project 'OBTableViewController'.
properties - Displays the properties of root project 'OBTableViewController'.
tasks - Displays the tasks runnable from root project 'OBTableViewController'.

HockeyApp tasks
---------------
hockeyapp - Uploades the app (.ipa, .dsym) to HockeyApp
hockeyappClean - Cleans up the generated files from the hockeyapp target

HockeyKit tasks
---------------
hockeykit - Creates a build that can be deployed on a hockeykit Server
hockeykitArchive - Prepare the app bundle so that it can be uploaded to the Hockeykit Server
hockeykitClean - Cleans up the generated files from the hockey target
hockeykitImage - Creates the image that is used on the HockeyKit Server
hockeykitManifest - Creates the manifest that is needed to deploy on a HockeyKit Server
hockeykitNotes - Creates the releasenotes.html and includes the notes that can be deployed to the HockeyKit Server

SimulatorsList tasks
--------------------
simulatorInstallApp - Install app on iOS Simulators
simulatorKill - Deletes contents and settings for all Simulators
simulatorRunApp - Install app on iOS Simulators
simulatorsClean - Deletes contents and settings for all iOS Simulators
simulatorsCreate - Delete and creates all iOS Simulators
simulatorsList - List all available Simulators
simulatorStart - Start iOS Simulators

Verification tasks
------------------
check - Runs all checks.

Xcode tasks
-----------
archive - Prepare the app bundle that it can be archive
infoplistModify
keychainClean - Cleanup the keychain
keychainCreate - Create a keychain that is used for signing the app
keychainRemove - Removes the gradle keychain from the search list
package - Signs the app bundle that was created by the build and creates the ipa
packageReleaseNotes - Creates release notes when building Mac Apps with Sparkle
provisioningClean
provisioningInstall - Installs the given provisioning profile
xcodebuild - Builds the Xcode project
xcodebuildClean - Cleans up the generated files from the previous build
xcodebuildConfig - Parses the xcodeproj file and setups the configuration for the build
xcodebuildForTest - Build the xcode project and the tests. A testbundle is created that contains the result.
xcodetest - Runs the unit tests for the Xcode project
xcodetestrun - Create a build for test of the Xcode project

Other tasks
-----------
test
</code>
</pre>


### Need More Help

For more information see the [Readme on Github](https://github.com/openbakery/gradle-xcodePlugin/blob/master/README.md)  
A full descripton of all parameters can be found in the [parameters documentation on Github](https://github.com/openbakery/gradle-xcodePlugin/blob/master/Documentation/Parameters.md)
