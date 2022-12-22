# LoadBalancer service

## Create a service

```$bash
kubectl apply -f loadbalancer.yaml
```

## Create a deployment

```$bash
kubectl apply -f deploy-app.yaml
```

## Get pod list

```$bash
kubectl get pods -o wide
kubectl get svc
```

## Get the node ip public address

```$bash
kubectl get pods -o wide
```

## Get the service ip public address

```$bash
kubectl get service -o wide
```

## Delete deployment

```$bash
kubectl delete -f deploy-app.yaml
```

## Delete service

```$bash
kubectl delete -f loadbalancer.yaml
```
