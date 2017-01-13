Jenkins slave with Oracle Java development environment
======================================================

Start a [Jenkins swarm](https://wiki.jenkins-ci.org/display/JENKINS/Swarm+Plugin) slave into docker with Oracle Java Development Kit (JDK) and Maven.

## Start a slave

   `docker run -d heliostech/jenkins-slave-java:8 -master http://jenkins-server/ -username JENKINS_USER -password JENKINS_USER_KEY -executors 2 -labels "linux java java8"`

### Configure the job to use the slave
On the jenkins job configuration page, check the box "Restrict where this project can be run" and set the "Label expression" to a label assigned to the node (e.g., linux && java8)

### Inject docker environment to the job
You need the plugin [EnvInject Plugin](https://wiki.jenkins-ci.org/display/JENKINS/EnvInject+Plugin) installed on the jenkins master.

Select "Inject environment variables to the build process" and set the "Properties File Path" to `/etc/docker.properties`

## Available Options

   Display the available options with the following command:

   `docker run -it --rm heliostech/jenkins-slave-java:8 -help`


## Credits

   This container is part of [DevStack](https://www.devstack.com/), a project to facilitate DevOps work with continuous integration and deployment environment ready to use.
