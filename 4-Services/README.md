# Services in kubernetes

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
kubectl apply -f vote-app-pod.yaml
```

4. create vote app service

```
kubectl apply -f vote-app-service.yaml
```

Now we want to register people using the /register endpoint and store the names in the redis db pods using the services.

5. Check the url of the vote-app service 

```
minikube service vote-app-svc  --url
```
6. now we can connect using the url we get in step 5

```
curl {url}/register
```