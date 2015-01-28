Jenkins plugin for Dokku
------------------------

Project: https://github.com/progrium/dokku

Installation
------------
```
cd /var/lib/dokku/plugins
git clone https://github.com/alessio/dokku-jenkins jenkins
dokku plugins-install
```

Commands
--------
```
$ dokku help
    jenkins:info             Display container information
    jenkins:logs             Display last logs from Jenkins container
    jenkins:start            Start Jenkins
    jenkins:stop             Stop Jenkins
```

Usage
-----

Start Jenkins:
```
$ dokku jenkins:start
Jenkins has started

       Host: 10.0.3.159
       Public port: 8080
       Public port for attached slave agents: 50000

```

Inspect container's logfile:
```
$ dokku jenkins:logs
2015-01-28T09:18:27.658790619Z /usr/share/jenkins/ref/init.groovy.d/tcp-slave-angent-port.groovy
2015-01-28T09:18:27.667692697Z  /usr/share/jenkins/ref/init.groovy.d/tcp-slave-angent-port.groovy -> init.groovy.d/tcp-slave-angent-port.groovy
2015-01-28T09:18:27.667817292Z copy init.groovy.d/tcp-slave-angent-port.groovy to JENKINS_HOME
2015-01-28T09:18:28.219838149Z Running from: /usr/share/jenkins/jenkins.war
2015-01-28T09:18:28.225358960Z webroot: EnvVars.masterEnvVars.get("JENKINS_HOME")
2015-01-28T09:18:28.614153281Z Jan 28, 2015 9:18:28 AM winstone.Logger logInternal
2015-01-28T09:18:28.614153281Z INFO: Beginning extraction from war file
2015-01-28T09:18:29.994872790Z Jan 28, 2015 9:18:29 AM org.eclipse.jetty.util.log.JavaUtilLog info
2015-01-28T09:18:29.994872790Z INFO: jetty-winstone-2.8
2015-01-28T09:18:32.285196787Z Jan 28, 2015 9:18:32 AM org.eclipse.jetty.util.log.JavaUtilLog info
2015-01-28T09:18:32.285196787Z INFO: NO JSP Support for , did not find org.apache.jasper.servlet.JspServlet
2015-01-28T09:18:33.166819441Z Jenkins home directory: /var/jenkins_home found at: EnvVars.masterEnvVars.get("JENKINS_HOME")
```

Stop a running Jenkins container:
```
$ dokku jenkins:stop
Jenkins has stopped.
```
