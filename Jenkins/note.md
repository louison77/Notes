# Jenkins

## Principles

* Jenkins is an open-source project written in Java.
* It is an software development automatisation tool. It can automate build, test and deployment for example.
* The application can be executed as a Java service, docker container, ... After installation Jenkins is running as a daemon service.
* There is a web GUI that can help configure the pipelines.
* It exists different plugins to help to accelerate the deployment process.
* Jenkins is more useful for Java Project.
* Jenkins is integrated with test and reporting tools.
* Jenkinsfile are written in Groovy language. These files are used to write Jenkisn Pipelines.

## Main commands

## Good practices and tips

* Jenkins web application is located by default on the port 8080.
* When launching the first time Jenkins on the application, an admin password is required. This password is located at `/var/lib/jenkins/secrets/initialAdminPassword`.
* Jenkins is based on a master/agent model. The master give task to agents that are installed on the target platforms ( ex: VM, Container, ... ). But it is possible that the master executes tasks without agents. It is the default behavior.
* Be careful to indicate the exact path of the Jenkinsfile when a pipeline trigger a scm repository.
