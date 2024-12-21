![image](https://github.com/user-attachments/assets/d97e64eb-c7cf-436d-9e7f-6be067c88438)## Kubernetes Architecture

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

##What is ETCD ? 
etcd : is the central source of truth in Kubernetes, storing all configuration and state information for the cluster.

###Basic Example:
When you create a new pod or service in Kubernetes, the kube-apiserver stores that information in etcd. For example:

You create a new Pod.
The kube-apiserver writes the desired state of that Pod to etcd.
Other components, like the kube-scheduler, read from etcd to determine where to schedule the Pod.



