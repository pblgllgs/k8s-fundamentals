# Replica sets

## Create a RS

```$bash
kubectl apply -f rs-example.yaml
```

## Get pod list

```$bash
kubectl get pods -o wide
```

## Get replica set name

```$bash
kubectl get rs
```

## Describe replica sest

```$bash
kubectl describe rs rs-example
```

## Delete replica

```$bash
kubectl delete -f rs-example.yaml
```
