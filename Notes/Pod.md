Pod has four major fields in yml manifest. Root level property. 
also these are the required fields in the yml manifest file.
1. apiVersion 
2. kind # kind refers what kind of object we want to refer like Pod, Service
3. metadata
4. spec


```sh
apiVersion: v1   #takes string
kind: Pod # takes string
metadata: # metadata is a dictionary
    name: 
    labels: # is a dictionary
        app: 
        type:
spec: # is a dictionary
    containers: # is a list or array
        # - dash refers the first item in the list
        - name: nginx-workload
          image: nginx:1.25.3



```

## Pod
Some of the workload controller which manages pod,
workload controllers are working on,
1. Deployment
2. StatefulSet
3. DaemonSet
4. Job
5. CronJob

All pods can communicate with all other pods, whether they are on the same node or on different nodes.
Pods can communicate with each other directly, without the use of proxies or address translation (NAT).