# deployment

sketch-app-deployment

### Create Charts for each service

```sh
cd charts
helm create charts/frontend
```

- Repeat for others

### Start minikube

```sh
minikube start
```

### Set context for kubectl

```sh
kubectl config use-context minikube
```

### Check cluster and nodes

```sh
kubectl cluster-info
kubectl get nodes
```

### Dry run local test

```sh
helm install frontend ./charts/frontend --dry-run --debug
helm install frontend ./charts/frontend --dry-run --debug --kubeconfig ~/.kube/config
```

### Stop minikube

```sh
minikube stop
minikube delete
minikube start
```
