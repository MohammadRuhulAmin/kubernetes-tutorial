Node Selector

Labiling Node First:

```sh
kubectl label nodes <node-name> <label-key>=<label-value>
kubectl label nodes node-1 size=Large
```

```sh
apiVersion: v1
kind: Pod
metadata:
    name: node-selector
spec:
    containers:
    - name: data-processor
      image: data-processor
    nodeSelector: 
        size: Large # But before attaching size = Large i must have lable the node "Large" before creating pod


```

But using Node Selector I cannot, deploy a pod depending on multiple condition, like Large or Medium, or 
Large or mini-Large etc. Thats why node affinity concept comes to the point. 
Mainly you cannot apply any condition in Node Selector. 

