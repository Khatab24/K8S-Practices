## Kubernetes Architecture
```scss
// Kubernetes Master Node Architecture
Master Node
├── etcd
├── kube-apiserver
├── kube-scheduler
├── kube-controller-manager
└── Add-ons
    ├── CoreDNS
    ├── kube-proxy
    └── Other components (e.g., monitoring or logging tools)

// Worker Node Architecture
Worker Node
├── kubelet
├── kube-proxy
└── Container Runtime (Docker, containerd, etc.)

```
![k1](https://github.com/user-attachments/assets/01eec61f-e5af-467a-85b7-696bef67b78e)



## Kubernetes Master Node Architecture

```scss
Master Node
├── etcd
├── kube-apiserver
├── kube-scheduler
├── kube-controller-manager
└── Add-ons
    ├── CoreDNS
    ├── kube-proxy
    └── Other components (e.g., monitoring or logging tools)
```

## 1-What is ETCD ? 
etcd : is the central source of truth in Kubernetes, storing all configuration and state information for the cluster.

### Basic Example:
When you create a new pod or service in Kubernetes, the kube-apiserver stores that information in etcd. For example:
You create a new Pod.
The kube-apiserver writes the desired state of that Pod to etcd.
Other components, like the kube-scheduler, read from etcd to determine where to schedule the Pod.
![k2](https://github.com/user-attachments/assets/4998c55b-82fb-42c5-b578-af310cd8ce14)

## 2-kube-apiserver
is the central control plane component that exposes the Kubernetes API and manages interactions with the cluster.
It handles authentication, authorization, request processing, and communicates with etcd for storing the cluster state.
It ensures that the desired state of the cluster is maintained and makes it accessible to users and other components in the system.
![image](https://github.com/user-attachments/assets/d638aca4-05e4-4f0f-abc4-e60f4e927d11)

## 3-kube-controller-manager
is one of the core components of the Kubernetes control plane responsible for maintaining the desired state of the cluster by running controller processes. Each controller watches for changes to specific resources in the cluster (like Pods, Deployments, Nodes, etc.) and takes actions to ensure that the cluster's current state matches the desired state.
## How the kube-controller-manager Works:
# Cluster State Check: The controller-manager continually monitors the current state of the cluster by reading information from the API server and etcd.
# Desired State: Based on the configuration of the resources (e.g., Deployments, ReplicaSets), the controller-manager knows the desired state of each resource.
# Reconciliation: If the actual state diverges from the desired state, the appropriate controller takes action to bring the system back to the desired state. This is known as reconciliation.
![image](https://github.com/user-attachments/assets/9b743bba-2f90-4434-9975-fef45571d342)

## 4-kube-scheduler 
is a core component of the Kubernetes control plane that is responsible for scheduling Pods onto nodes in the cluster. It makes decisions about which node in the cluster a newly created or unscheduled Pod should run on based on various factors such as resource availability, constraints, and policies.
![image](https://github.com/user-attachments/assets/dbaced5d-f74c-4cd2-86af-bb3002f3ae9e)

```scss
Worker Node
├── kubelet
├── kube-proxy
└── Container Runtime (Docker, containerd, etc.)
```
## 1-kubelet
core component in Kubernetes that manages the state of Pods and containers on a node. It ensures that containers are running and healthy, interacting with the container runtime and the Kubernetes control plane to report status and act on requests for resource allocation, health checks, and scheduling.
![image](https://github.com/user-attachments/assets/1811db4b-48a0-4b34-96aa-b425da97a835)

## 2-kube-proxy
vital component that helps manage networking within a Kubernetes cluster. It handles the routing of traffic to the right Pods based on service configurations, providing load balancing and network rule management, making it essential for the cluster's overall network functionality.
![image](https://github.com/user-attachments/assets/48a1f30f-b9e2-4394-adaf-ff6e48ad14e9)








