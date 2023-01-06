# Secrets

## Create secrets

```$bash
kubectl apply -f secrets.yaml
```

## Get cm

```$bash
kubectl get secret
kubectl describe secret secrets
kubectl get secret secrets -o YAML
```

## Create a pod

```$bash
kubectl apply -f pod.yaml
```

## Connect docker container

```$bash
kubectl exec  -it mybox -- /bin/sh
echo $username
echo $password
exit
```

## Delete pv

```$bash
kubectl delete -f secrets.yaml
```

## Delete pvc

```$bash
kubectl delete -f pod.yaml --force --grace-period=0
```
