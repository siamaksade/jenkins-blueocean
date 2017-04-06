# Jenkins Blue Ocean for OpenShift
This repository is meant to be used with Jenkins S2I on OpenShift to 
install and enable Blue Ocean plugin on the official Jenkins image provided
in OpenShift.

Create a Jenkins S2I build with this GitHub repository:
```
oc new-build jenkins:2~https://github.com/siamaksade/jenkins-blueocean.git --name=jenkins-blueocean
```

Then you can deploy the Jenkins templates with the customized image:
```
oc new-app jenkins-ephemeral -p NAMESPACE=_NAMESPACE_ -p JENKINS_IMAGE_STREAM_TAG=jenkins-blueocean:latest 
```