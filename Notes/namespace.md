Type of Namespace: 
------------------
1. kube-system
2. default
3. kube-public

```sh
apiVersion: v1
kind: Namespace
metadata:
  name: dev

```

default set any custom namespace in k8s:

```sh
kubectl config set-context $(kubectl config current-context) --namespace=dev
```

