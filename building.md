+++
title = "Building"
url = "gxp/building.html"

[menu.gxp]
name = "Building"
weight = 10 
+++


The simplest build configuration that you can use in your `build.gradle` looks like the following one that was using in the [Getting Started](getting-started.html) guide:

```
plugins {
	id "org.openbakery.xcode-plugin" version "0.14.+"
}

xcodebuild {
	target = 'Example'
}
```

With this configuration you can compile your app for for the iOS simulator but when you also want to execute the unit test you need to specify the scheme that has unit test configured:

```
xcodebuild {
	target = 'Example'
	scheme = 'Example'
}
```



(Note: This site is work in progress...)