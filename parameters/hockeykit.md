+++
title = "hockeykit"
url = "gxp/parameters/hockeykit.html"
class = "parameters"

[menu.gxp]
name = "hockeykit"
parent = "Parameters"
weight = 60
+++

The `hockeykit` parameters are used to prepare a IPA for ad hoc deployment using [HockeyKit](https://github.com/bitstadium/HockeyKit)

e.g.

```
hockeykit {
	displayName='MyExample'
}
```

# Parameters


### displayName

Title that should be used that is shown on the hockeykit site for the app.
  If the value is not set then the bundle identifier is used

default value: the CFBundleDisplayName from the Info.plist file is used


### versionDirectoryName

subdirectory that should be used for the app.

default value: `0`


### outputDirectory

directory where to store the files that are generated for the hockeykit distribution

default value: `'build/hockeykit'`


### notes

Release notes as HTML or Markdown for the build that is stored in a releasenotes.html.

default value: _empty_
