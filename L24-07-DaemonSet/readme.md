# Daemonset

## Create a daemonset

```$bash
kubectl apply -f daemonset.yaml
```

## Get pod list

```$bash
kubectl get pods --selector=app=daemonset-example -o wide
```

## Delete deployment

```$bash
kubectl delete -f daemonset.yaml
```
