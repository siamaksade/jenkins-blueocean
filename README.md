# Jenkins Blue Ocean for OpenShift
This repository is meant to be used with Jenkins S2I on OpenShift to 
install and enable Blue Ocean plugin

```
oc new-build jenkins:2~https://github.com/siamaksade/jenkins-blueocean.git --name=jenkins-blueocean4
```
