Jenkins swarm slave with Ansible development environment
========================================================

Start a [Jenkins swarm](https://wiki.jenkins-ci.org/display/JENKINS/Swarm+Plugin) slave with the latest development version of Ansible installed in Docker.

### Start a slave

```
docker run \
  --detach \
  patrickmslatteryvt/docker-jenkins-slave:devel-2.2.0 \
  -master http://jenkins-server/ \
  -username JENKINS_USER \
  -password JENKINS_USER_KEY \
  -executors 2 \
  -labels "linux ansible 2.2.0"
```

### Available Options

Display the available options with the following command:

```
docker run -it --rm patrickmslatteryvt/docker-jenkins-slave -help
```
