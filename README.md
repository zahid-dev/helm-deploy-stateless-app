# Dploying a NodeJS App with MongoDB using HELM

## Introduction:
Helm chart provides an easy method of deploying kubernetes resources. This application is a NodeJS app with mongo DB setup in a high available and fault tolerant manner, hosted on kubernetes.

## Application:
Application is a NodeJS easy notes app that makes use of mongoDB. I have used nginx to serve the app and calico plugin to ensure mongoDB Pod does not talk to any other POD except the app one.

## High Availability and Fault Tolerance:
Kubernetes being a mature and powerful orchestration engine, offer a wide variety of high available and fault tolerant infrastructure configuration. We can run multi node setups, both master and worker nodes(upto 3 recommended). But for the sake of this task, I have introduced redundancy only at Pod level(ensuring 3 replicas). We can deploy metrics server and configure horizontal pod autoscalar on it. We can deploy prometheus with graphana monitoring that can further enhance our debugging and monitoring capabilities. There are a lot of possibilities to ensure maximum availability. Depends purely on the use case. Redundancy can be inroduced at the datacenter to datacenter level or even multi region support with the help of cloud providers. In fact kubernetes now supports redundancy and high availability configuration in most of the infrastructure components, which makes it even more powerful to cater the diverse business needs and support ideas.


