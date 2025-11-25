
Imperative vs Declarative Approach Kubernetes:

imperative command approach:
```sh
    kubectl run --image=nginx nginx
    kubectl create -f nginx.yml
    kubectl delete -f nginx.yml
    kubectl replace -f nginx.yml
    kubectl edit deployment nginx
```

declarative command approach:

```sh
# nginx.yml is also known as object configuration file
kubectl apply -f nginx.yml

```