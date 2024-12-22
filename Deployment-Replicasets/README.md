## ReplicaSet
is a resource that ensures a specified number of identical Pods are running at any given time. Its primary function is to maintain the desired number of Pod replicas, automatically creating or deleting Pods as necessary to match the defined count. 

### What is Kubernetes ReplicaSets?
https://www.youtube.com/watch?v=eGjiK6YeuX8&t=3s


## Deployment
is a higher-level abstraction that manages the deployment and scaling of a set of Pods, typically by overseeing ReplicaSets. It provides declarative updates to applications
![image](https://github.com/user-attachments/assets/d8c6726f-47a6-43e2-b032-fd8659d47d9e)

### Key Features of Deployments:
Declarative Updates: You specify the desired state in a Deployment, and Kubernetes ensures that the actual state matches it. 
KUBERNETES

Rolling Updates: Deployments support rolling updates, allowing for zero-downtime updates to applications by incrementally replacing Pods with new ones. 
KUBERNETES
![image](https://github.com/user-attachments/assets/8b6441dc-add4-42a0-b609-d1726aefb5ea)

Rollback: If an update causes issues, Deployments can revert to a previous stable state, ensuring application stability. 
KUBERNETES
![image](https://github.com/user-attachments/assets/1f80f4a1-a076-4806-a2cf-a3ab847c2832)


Scaling: Deployments facilitate scaling the number of replicas up or down to accommodate changes in load.

![image](https://github.com/user-attachments/assets/26126d6e-0d31-48e5-9a9b-9a2de50df018)
