Controller:is the brain of Kubernetes. 
one is Replication Controller. 

What is the use of Replication Controller ?

```sh
apiVersion: v1
kind: ReplicationController
metadata:
  name: myapp-rc
  labels:
    app: myapp
    type: frontend-application

spec: #this is the specification of replication controller
  replicas: 3 # total number of pod 
  template:
    metadata:
      name: myapp-pod
      labels:
        app: myapp
        type: front-end
    spec:
      containers:
      - name: nginx-container
        image: nginx



```
# kubectl get replicationController
If we use ReplicaSet, we have to define the selector. 

kubectl create -f replicaset-definition.yml  # to create a Replicaset
kubectl replace -f replicaset-definition.yml # to update replicaset
kubeclt delete replicaset <file-name>
kubectl scale -replicas=6 -f replicaset-definition.yml # to scale in runtime, not updating the file
