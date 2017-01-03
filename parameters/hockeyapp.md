+++
title = "hockeyapp"
url = "gxp/parameters/hockeyapp.html"
class = "parameters"

[menu.gxp]
name = "hockeyapp"
parent = "Parameters"
weight = 60
+++

The `hockeyapp` parameters are used to prepare a IPA for ad hoc deployment using [HockeyApp](https://hockeyapp.net)

e.g.

```
hockeyapp {
	apiToken='12345678901234567890123456789012'
	apiToken='abcdefghijklmnopqrstuvwxyzabcdef'
}
```


## HockeyApp Parameters

### apiToken

The HockeyApp API Token (see https://rink.hockeyapp.net/manage/auth_tokens )

default value: _empty_

### appID

The HockeyApp App ID (see https://rink.hockeyapp.net/manage/dashboard and select the app)

default value: _empty_

### outputDirectory

Optional, output directory where the ipa an dSYM.zip is created

  default value: "build/hockeyapp"

### notes

Release notes for the build

  default value: "This build was uploaded using the gradle xcodePlugin"

### status

Optional, download status (can only be set with full-access tokens):

  default value: 2

### notify

Optional, notify testers

  default value: 1

### notesType

Optional, type of release notes

  default value: 1

### teams

Optional, corresponds to `teams` (http://support.hockeyapp.net/kb/api/api-apps)

default value: _empty_  
  example value: `[1231, 123]`

### users

Optional, corresponds to `users` (http://support.hockeyapp.net/kb/api/api-apps)

default value: _empty_  
  example value: `[1231, 123]`

### tags

Optional, corresponds to `tags` (http://support.hockeyapp.net/kb/api/api-apps)

default value: _empty_  
  example value: `['earlytesters', 'mytag2']`

### mandatory

Optional, set 1 to make version as mandatory (http://support.hockeyapp.net/kb/api/api-apps)

  default value: 0

### releaseType

Optional, set the release type as in `release_type` (http://support.hockeyapp.net/kb/api/api-apps)

  default value: 1

### privatePage

Optional, set true for a private download page as in `private` (http://support.hockeyapp.net/kb/api/api-apps)

  default value: false

### commitSha

Optional, corresponds to `commit_sha` (http://support.hockeyapp.net/kb/api/api-apps)

default value: _empty_

### buildServerUrl

Optional, corresponds to `build_server_url`

default value: _empty_

### repositoryUrl

Optional, corresponds to `repository_url`

default value: _empty_
