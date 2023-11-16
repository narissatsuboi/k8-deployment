# k8-deployment

## Description

k8-deployment contains kubernetes configuration files to deploy pods and services for a simple web application with a database on a local cluster

## Prerequisites

- minikube or Docker Desktop Kubernetes cluster

## Logical View

![logical view](/assets/logical_view.png)

## Config View

![configuration view](/assets/configuration_view.png)

## Usage

1. Mongo config file and secret. 
`$ kubectl apply -f mongo-config.yaml`
`$ kubectl apply -f mongo-secret.yaml`


2. Mongo deployment and internal service. 
`$ kubectl apply -f mongo.yaml`

3. Webapp deployment and external service. 
`$ kubectl apply -f webapp.yaml`

4. Get node IP. 
`kubectl get node`

5. Curl to exposed port. 
`curl http://<nodeIP>:<nodePort>` or `curl http://localhost:<nodePort>`

6. View all. 
`$ kubectl get all`
![get_all](/assets/get_all.png)

## Credits
This repo is an annotated version of the K8 tutorial from [TechWorld by Nana][1]. 
- [Kubernetes Crash Course for Absolute Beginners][2] on YouTube. 

[1]: https://www.techworld-with-nana.com/
[2]: https://www.youtube.com/watch?v=s_o8dwzRlu4
