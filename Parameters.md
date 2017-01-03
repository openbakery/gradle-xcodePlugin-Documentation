+++
title = "Parameters"
url = "gxp/parameters.html"
class = "parameters"

[menu.gxp]
Name = "Parameters"
Weight = 20 
+++


Here you find all parameters that are available for the Xcode Build Plugin.

#### The structure of the parameters

* [xcodebuild](parameters/xcodebuild.html)
 * [signing](parameters/signing.html)
 * [infoplist](parameters/infoplist.html)
* [coverage](parameters/coverage.html)
* [oclint](parameters/oclint.html)
* [appstore](parameters/appstore.html)
* [hockeykit](parameters/hockeykit.html)
* [hockeyapp](parameters/hockeyapp.html)
* [crashlytics](parameters/crashlytics.html)



Example `build.gradle` file:

```
xcodebuild {
	target = "Example"
	scheme = "Example"
	
	signing {
		certificateURI = 'file:///Users/me/codesign/development.p12'
		certificatePassword = 'my_secret_password'
		mobileProvisionURI = [
			file:///Users/me/codesign/com.example.Example.mobileprovision',
		]
	}
	infoplist {
		bundleDisplayName = "MyApplication"
	}
  
	destination = project.ext.destination
}


coverage {
	outputFormat = 'html'
	exclude = 'Pods.*'
}

oclint {
	maxPriority2 = 100
	maxPriority3 = 200			
}

appstoreUpload {
	username = "My-Apple-ID"
	password = "My-Appstore-Password"
}


```