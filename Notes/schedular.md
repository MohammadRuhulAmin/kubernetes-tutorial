Assigning a `nodeNode` is the easiest way to make a pod schedule.

For Scheduling a newly assigned pod to a node. 
```sh
apiVersion: v1
kind: Pod
metadata:
    name: nginx
    labels:
        name: nginx
spec:
    containers:
    - name: nginx
      image: nginx:1.25.3
    nodeName: node01

```

For Scheduling an existing pod to a node

```sh
apiVersion: v1
kind: Binding
metadata:
  name: nginx
target:
  apiVersion: v1
  kind: Node
  name: node02

curl --header "Content-Type: application/json" \
     --request POST \
     --data '{"apiVersion":"v1","kind":"Binding","metadata":{"name":"nginx"},"target":{"apiVersion":"v1","kind":"Node","name":"node02"}}' \
     http://$SERVER/api/v1/namespaces/default/pods/$PODNAME/binding/
```

We cannot move a running pod from one node to another node. 