# liveness

## Create a pod

```$bash
kubectl apply -f pod.yaml
```

## Describe pod

```$bash
kubectl describe pod liveness-example
```

## Delete pvc

```$bash
kubectl delete -f pod.yaml --force --grace-period=0
```
