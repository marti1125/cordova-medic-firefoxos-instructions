# cordova-medic-firefoxos
Instructions for implement FirefoxOS in cordova-medic

Files                    | Directories
------------------------ | -------------
master_buildbot0810.cfg  | master/
cordova.conf             | master/
build_firefoxos.js       | master/
cordova-config.json      | master/
cordova-repos.json       | master/
build_firefoxos.js       | master/src/build/makers

# BuildBot 0.8.10

Some error if you run: $ buildbot start master

*exceptions.DeprecationWarning: buildbot.steps.shell.SetProperty was deprecated in Buildbot 0.8.8: It has been renamed to SetPropertyFromCommand

exceptions.DeprecationWarning: buildbot.steps.source.SVN was deprecated in Buildbot 0.8.9: The slave-side SVN step is deprecated and will be removed in a future version.  Please switch to the corresponding master-side step.

exceptions.DeprecationWarning: buildbot.steps.source.Git was deprecated in Buildbot 0.8.9: The slave-side Git step is deprecated and will be removed in a future version.  Please switch to the corresponding master-side step
*

master_buildbot0810.cfg corrects these issues

[https://issues.apache.org/jira/browse/CB-8489](https://issues.apache.org/jira/browse/CB-8489)