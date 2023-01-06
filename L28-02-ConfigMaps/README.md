# ConfgiMaps

## Create configMap

```$bash
kubectl apply -f cm.yaml
```

## Get cm

```$bash
kubectl get cm
kubectl describe configmap cm-example
```

## Create a pod

```$bash
kubectl apply -f pod.yaml
```

## Connect docker container

```$bash
kubectl exec  -it mybox -- /bin/sh
echo $CITY
echo $STATE
exit
```

## Delete pv

```$bash
kubectl delete -f cm.yaml
```

## Delete pvc

```$bash
kubectl delete -f pod.yaml --force --grace-period=0
```
