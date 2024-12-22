## 1-manual scheduling
refers to the process of assigning Pods to specific Nodes without relying on the default scheduler.

## 2-taints and tolerations
work together to control how Pods are scheduled onto Nodes, ensuring that certain Pods are either repelled from or attracted to specific Nodes based on defined criteria.

#### A taint consists of three parts:
Key: Identifier for the taint.
Value: Optional descriptor for the taint.
  ##### Effect: Determines the taint's impact on Pod scheduling, which can be:
NoSchedule: Prevents Pods without matching tolerations from being scheduled on the Node.
PreferNoSchedule: Prefers not to schedule Pods without matching tolerations on the Node but doesn't enforce it strictly.
NoExecute: Evicts existing Pods without matching tolerations and prevents new ones from being scheduled.

    ```scss
    kubectl taint nodes gpu-node special=true:NoSchedule ```


#### A toleration includes:

Key: Matches the taint's key.
Operator: Defines the relationship between the key and value (Equal or Exists).
Value: Matches the taint's value.
Effect: Matches the taint's effect.

##### What is taint and toleration 
[text](https://youtu.be/yFmgW3qoaFY)

## 3-Node Selectors
is a simple mechanism that allows you to constrain Pods to run only on Nodes with specific labels. By specifying a nodeSelector field in a Pod's specification, you can ensure that the Pod is scheduled only onto Nodes that match the defined key-value pair labels. 
KUBERNETES

```scss
kubectl label nodes node-01 disktype=ssd
```


## 4-node affinity
is a feature that allows you to control which nodes your Pods are eligible to be scheduled on, based on node labels. It provides more expressive and flexible placement constraints compared to the simpler nodeSelector

# Types of Node Affinity:

#      Required During Scheduling, Ignored During Execution (requiredDuringSchedulingIgnoredDuringExecution):

Behavior: Specifies rules that must be met for a Pod to be scheduled onto a node. If no available nodes satisfy these rules, the Pod will not be scheduled. Once the Pod is running, changes to node labels that violate these rules do not affect the Pod.

#     Preferred During Scheduling, Ignored During Execution (preferredDuringSchedulingIgnoredDuringExecution):

Behavior: Indicates a preference for scheduling the Pod onto nodes that meet certain criteria. The scheduler will try to place the Pod on a preferred node, but if none are available, it will schedule the Pod on a non-preferred node. As with the required type, changes to node labels after scheduling do not impact the Pod.

```scss
kubectl label nodes <node-name> disktype=ssd
```




