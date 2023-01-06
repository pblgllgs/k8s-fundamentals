# Persistent Volume and claim

## Create a volume

```$bash
kubectl apply -f pv.yaml
```

## Get pv

```$bash
kubectl get pv
```

## Create a pvc

```$bash
kubectl apply -f pvc.yaml
```

## Get pvc

```$bash
kubectl get pvc
```

## Create a pod

```$bash
kubectl apply -f pod.yaml
```

## Get the pod information

```$bash
kubectl describe po mybox
```

## Connect docker container

```$bash
kubectl exec  -it mybox -- /bin/sh

ls
cat > hello.txt
Hello world
enter
ctl-D
cat hello.txt
exit
```

## Delete pod first time

```$bash
kubectl delete -f pod.yaml --force --grace-period=0
```

## Create a new pod

```$bash
kubectl apply -f pod.yaml
```

## Connect docker container again

```$bash
kubectl exec  -it mybox -- /bin/sh

cd demo
cat hello.txt
exit
```

## Delete pv

```$bash
kubectl delete -f pv.yaml
```

## Delete pvc

```$bash
kubectl delete -f pvc.yaml
```

## Delete pod

```$bash
kubectl delete -f pod.yaml --force --grace-period=0
```
