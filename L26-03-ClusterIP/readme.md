# ClusterIP service

## Create a service

```$bash
kubectl apply -f clusterip.yaml
```

## Create a deployment

```$bash
kubectl apply -f deploy-app.yaml
```

## Create a pod

```$bash
kubectl apply -f pod.yaml
```

## Get pod list

```$bash
kubectl get pods -o wide
kubectl get svc
```

## Connect to the bysybox container

```$bash
kubectl exec -it mybox -- /bin/sh
```

## Get the nginx home page from busybox

```$bash
wget -qO- http://svc-example:8080

exit
```

## Delete deployment

```$bash
kubectl delete -f deploy-app.yaml
```

## Delete pod

```$bash
kubectl delete -f pod.yaml
```

## Delete service

```$bash
kubectl delete -f clusterip.yaml
```
