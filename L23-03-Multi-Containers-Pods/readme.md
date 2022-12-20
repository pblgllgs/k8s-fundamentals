# Pod Multicontainers

```$bash
kubectl apply -f two-containers.yaml  
```

```$bash
kubectl get pods -o wide
```

```$bash
kubectl describe pod two-containers
```

```$bash
kubectl exec -it two-containers -c mybox -- /bin/sh
```

```$bash
wget -qO- localhost
```

```$bash
exit
```

```$bash
kubectl delete -f two-containers.yaml --force --grace-period=0
```
