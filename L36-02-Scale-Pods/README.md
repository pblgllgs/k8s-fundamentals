# liveness

## See the pods and find the metric server

```$bash
kubectl get po -n kube-system
```

## Deploy web-server

```$bash
kubectl apply -f deploy.yaml
```

## Get pods

```$bash
kubectl get pods
```

## Set the autoscaling limits

```$bash
kubectl autoscale deployment hps-deployment --cpu-percent=50 --min=1 --max=4
```

## Get hpa

```$bash
kubectl get hpa
```

## Deploy pod busybox

```$bash
kubectl apply -f pod.yaml
```

## Connect to the container

```$bash
kubectl exec -it mybox -- /bin/sh
```

## Test this endless loop

```$bash
while true; do wget -q -O- http://php-apache; done
```

## Deploy metrics server

```$bash
kubectl apply -f components.yaml
```

## Delete hpa

```$bash
kubectl delete hpa hpa-deployment
```

## Delete pod

```$bash
kubectl delete -f pod.yaml --force --grace-period=0
```

## Delete deploy

```$bash
kubectl delete -f deploy.yaml
```

## Delete server metrics

```$bash
kubectl delete -f components.yaml
```
