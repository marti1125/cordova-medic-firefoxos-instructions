# cordova-medic-firefoxos (in progress....)
Instructions for implement FirefoxOS in cordova-medic

Files                                          | Directories
---------------------------------------------- | -------------
master_buildbot0810.cfg (rename to master.cfg) | master/
cordova.conf                                   | master/
build_firefoxos.js                             | master/
cordova-config.json                            | master/
cordova-repos.json                             | master/
build_firefoxos.js                             | master/src/build/makers

###Instructions:

* $ buildbot create-master master
* Copy files according to the table
* Copy all content of cordova-medic to master/
* $ buildslave create-slave slave_firefoxos localhost:9889 cordova-firefoxos-slave pass
* $ buildbot start master
* $ buildslave start slave_firefoxos
* $ tail -f master/twistd.log


# BuildBot 0.8.10

Some error if you run: $ buildbot start master

*exceptions.DeprecationWarning: buildbot.steps.shell.SetProperty was deprecated in Buildbot 0.8.8: It has been renamed to SetPropertyFromCommand*

*exceptions.DeprecationWarning: buildbot.steps.source.SVN was deprecated in Buildbot 0.8.9: The slave-side SVN step is deprecated and will be removed in a future version.  Please switch to the corresponding master-side step.*

*exceptions.DeprecationWarning: buildbot.steps.source.Git was deprecated in Buildbot 0.8.9: The slave-side Git step is deprecated and will be removed in a future version.  Please switch to the corresponding master-side step*


master_buildbot0810.cfg corrects these issues

[https://issues.apache.org/jira/browse/CB-8489](https://issues.apache.org/jira/browse/CB-8489)
