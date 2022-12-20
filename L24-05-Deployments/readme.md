# Deployments

## Create a deployment

```$bash
kubectl apply -f deploy-example.yaml
```

## Get pod list

```$bash
kubectl get pods -o wide
```

## Describe de pod

```$bash
kubectl describe pod deploy-example
```

## Get deployment info

```$bash
kubectl get deploy
kubectl describe deploy deploy-example
```

## Get replicaset name

```$bash
kubectl get rs
kubectl describe rs
```

## Delete deployment

```$bash
kubectl delete -f deploy-example.yaml
```
