## Create a pod for the Vote App

```bash
    kubectl apply -f vote-app.yaml
```

## Start Minikube

```bash
    minikube ssh
```

## Check the ip of the created pod on minikube


```bash
    kubectl get pods -o wide
```

## Check the vote endpoint

```bash
    curl {pod_id}/vote
```