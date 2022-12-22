# Nodeport service

## Create a service

```$bash
kubectl apply -f nodeport.yaml
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
kubectl get nodes -o wide
```

## Delete deployment

```$bash
kubectl delete -f deploy-app.yaml
```

## Delete service

```$bash
kubectl delete -f nodeport.yaml
```
