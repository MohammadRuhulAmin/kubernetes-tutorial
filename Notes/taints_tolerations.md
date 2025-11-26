## Taints and Toleration
For worker nodes:
- ~Taints are set on Node~
- ~Toleration are set on Pods~

To taint the nodes
```sh
    # Set Taints 
    kubectl taint nodes node-name key=value:taint-effect
    kubectl taint nodes node1 app=myapp:NoSchedule
```
There Three Taint Effects:
1. NoSchedule
2. PreferNoSchedule
3. NoExecute

"Tolerations are added to pods"

```sh
apiVersion: v1
kind: Pod
metadata:
    name: my-app
spec:
    containers:
    - name: nginx-container
      image: nginx
    tolerations:
    - key: "app" # Value need to be encoded in ""
      operator: "Equal" # Value need to be encoded in ""
      value: "myapp" # Value need to be encoded in ""
      effect: "NoSchedule" # Value need to be encoded in ""


```
Master Nodes has all the capabilities for hosting pods + it runs all the management softwares. 
Kube-scheduler does not schedule any pod in the master-node. The best practise is not to deploy 
any workloads in master-node. 
```sh
    kubectl describe node kubemaster | grep Taint
```
Remove taint from control-plane
```sh kubectl taint nodes controlplane  node-role.kubernetes.io/control-plane:NoSchedule-```
