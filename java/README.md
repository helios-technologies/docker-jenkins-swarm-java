Jenkins slave with Java development environment
===============================================

Start a [Jenkins swarm](https://wiki.jenkins-ci.org/display/JENKINS/Swarm+Plugin) slave into docker with java jdk and maven.

## Start a slave

   `docker run -d heliostech/jenkins-slave-java -master http://jenkins-server/ -username JENKINS_USER -password JENKINS_USER_KEY -executors 2 -labels "linux java"`


## Available Options

   Display the available options with the following command:

   `docker run -it --rm heliostech/jenkins-slave-java -help`


## Credits

   This container is part of [DevStack](https://www.devstack.com/), a project to facilitate DevOps work with continuous integration and deployment environment ready to use.
