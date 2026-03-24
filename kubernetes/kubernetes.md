# Kubernetes

## Why do we need Kubernetes?
- Let's assume we have an enterprise application with more than 1000s of containers running in one virtual machine. For example, `SPOTIFY` runs on 65000 nodes with millions of containers. We can refer to Spotify Blogs. There maybe some containers that will fail in the virtual machines and we have devops engineer who will be responsible for restarting the containers. How do we manage this in a large scale?
- Some Challenges that a developer may face:
1. Scalability - Let's say there is an event in the application, how do we scale the application to handle the load?
2. Availability - Let's say there is a failure in the application, how do we make sure the application is available to the users?
3. Fault Tolerance - how will the application recover from the failure of a node or a container? Does it have auto-healing capabilities.
4. Management - How do we manage the application in a large scale? When do we need the more nodes or container and when do we need less?
5. Orchestration - How do we manage the application in a large scale? 

For the above challenges we use Kubernetes.

## What is Kubernetes?
- Kubernetes is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications.
- Kubernetes is a Greek word which means "helmsman" or "pilot".
