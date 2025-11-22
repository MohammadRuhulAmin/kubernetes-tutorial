to check my docker image from docker hub/docker registry: https://hub.docker.com/r/mdruhulamin/hello-node


kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
mi
change user: su - k8s
User permission: sudo usermod -aG docker k8s
create user: 
```sh
    adduser newUser
    usermod -aG sudo newUser
    su - newUser
```

user: k8s
pass: ruhulamin


host: 10.10.200.23
user: ruhul
passwd: );x#fUUtc%PW1Zo


targetPort does not work or cannot be used in Deployment / Pod. It only works on Service

