Core Concepts:
1. Cluster Architecture
2. Api Primitives
3. Services and other Networ premitives


1. Cluster Architecture
a. kubernetes Architecture b. etcd c. kube api d. controller manager 
e. kube schedular f. kubelet 

Muster Node has: 
1. etcd cluster
2. kube-scheduler
3. kube-apiserver
4. controller manager
Worker Node has:
1. kubelet
2. kube-proxy

docker and kubernetes are tightly coupled

etcd is a distributed, reliable key value data store that is simple, secure and fast.
it is used for small distributed metadata.

etcd stores the infromation in kubernetes:
1. nodes 2. pods 3. config 4. secrect 5. Account 6. Roles and bindings
Every additional upbdate on pods, services are updated in etcd database server.
