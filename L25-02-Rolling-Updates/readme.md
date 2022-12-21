# Deployment Rolling updates

## Create a deployment

```$bash
kubectl apply -f hello-deployment.yaml
```

## Get deployment status

```$bash
kubectl rollout status deployment/hello-dep
```

## Get pod list

```$bash
kubectl get pods -o wide
```

## Describe de deployment

```$bash
kubectl describe deploy hello-dep
```

## Get replicaset

```$bash
kubectl get rs
```

## Update version tag "k8sacademy/hello-app:2.0"

```$bash
kubectl apply -f hello-deployment.yaml
```

## Get deployment status again

```$bash
kubectl rollout status deployment/hello-dep
```

## Get pods list

```$bash
kubectl get pods -o wide
```

## ReplicaSets

```$bash
kubectl get rs
```

## Get deployment history

```$bash
kubectl rollout history deployment/hello-dep
```

## Undo the last deployment

```$bash
kubectl rollout undo deployment/hello-dep

o

kubectl rollout undo deployment/hello-dep --to-revision 1
```

## Delete deployment

```$bash
kubectl delete -f hello-deployment.yaml
```
