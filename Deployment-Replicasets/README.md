## ReplicaSet
is a resource that ensures a specified number of identical Pods are running at any given time. Its primary function is to maintain the desired number of Pod replicas, automatically creating or deleting Pods as necessary to match the defined count. 

### What is Kubernetes ReplicaSets?
https://www.youtube.com/watch?v=eGjiK6YeuX8&t=3s


## Deployment
is a higher-level abstraction that manages the deployment and scaling of a set of Pods, typically by overseeing ReplicaSets. It provides declarative updates to applications

### Key Features of Deployments:
Declarative Updates: You specify the desired state in a Deployment, and Kubernetes ensures that the actual state matches it. 
KUBERNETES

Rolling Updates: Deployments support rolling updates, allowing for zero-downtime updates to applications by incrementally replacing Pods with new ones. 
KUBERNETES

Rollback: If an update causes issues, Deployments can revert to a previous stable state, ensuring application stability. 
KUBERNETES

Scaling: Deployments facilitate scaling the number of replicas up or down to accommodate changes in load.

