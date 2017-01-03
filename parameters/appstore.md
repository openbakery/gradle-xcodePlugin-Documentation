+++
title = "appstore"
url = "gxp/parameters/appstore.html"
class = "parameters"

[menu.gxp]
name = "appstore"
parent = "Parameters"
weight = 30
+++

The `appstore` parameters are used when uploading a IPA to iTunesConnect and are needed for the AppStore tasks `appstoreUpload` and `appstoreValidate`. e.g.

```
appstore {
	username = "My-Apple-ID"
	password = "My-Appstore-Password"
}
```

# Parameters

### username

Your Apple ID

default value: _empty_

### password

The password for your Apple ID

default value: _empty_