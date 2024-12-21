## Kubernetes Architecture

```scss
// Kubernetes Master Node Architecture
Master Node
├── etcd
├── kube-apiserver
├── kube-scheduler
├── kube-controller-manager
├── cloud-controller-manager (if using cloud provider integration)
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


## Kubernetes Master Node Architecture

```scss
Master Node
├── etcd
├── kube-apiserver
├── kube-scheduler
├── kube-controller-manager
├── cloud-controller-manager (if using cloud provider integration)
└── Add-ons
    ├── CoreDNS
    ├── kube-proxy
    └── Other components (e.g., monitoring or logging tools)
```
