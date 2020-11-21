# Deployment in kubernetes

1. Create redis pod 
```
kubectl apply -f redis-db-pod.yaml
```
2. Create redis service 
```
kubectl apply -f redis-service.yaml
```

3. create vote app replica sets

```
kubectl apply -f vote-app-deployment.yaml
```

4. create vote app service

```
kubectl apply -f vote-app-service.yaml
```

5. Check the url of the vote-app service 

```
minikube service vote-app-svc  --url
```
6. Now we will try to hit the crash endpoint and break one of the pods

```
curl {url}/crash
```

we notice that as soon as the pod is crashed automatically a new deployment is created and replaced.

If we hit the crash endpoint multiple times then all the pods will break and we will not get any response for other endpoints untill new deployments are up
