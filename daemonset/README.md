## A DaemonSet 
is a Kubernetes controller that ensures a copy of a specific pod is running on all (or some) nodes in the cluster. It is typically used for deploying system-level applications that need to run on every node in a cluster, such as monitoring agents, log collectors, or networking components.

## Use Cases for DaemonSets
Logging: Deploying logging agents (like Fluentd or Logstash) on every node to collect logs from containers.
Monitoring: Running monitoring tools (like Prometheus Node Exporter) on every node to gather metrics.
Networking: Running network proxies or other system-level services on every node.
Backup/Restore: Running backup or restore processes on every node to ensure data integrity.

docs link https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/
