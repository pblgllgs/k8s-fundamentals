# Blue-Green Deployments

## Create a deployment v1

```$bash
kubectl apply -f hello-dep-v1.yaml
```

## Create a service

```$bash
kubectl apply -f clusterip.yaml
```

## Get pod list

```$bash
kubectl get pods -o wide
kubectl get svc
```

## Display app in the browser

```$bash
kubectl port-forward service/svc-front 8080:8080
```

## Create a deployment v2

```$bash
kubectl apply -f hello-dep-v2.yaml
```

## Get pod list after deploy v2

```$bash
kubectl get pods -o wide
```

## Change service label to "hello-v2"

```$bash
apiVersion: v1
kind: Service
metadata:
 name: svc-front
spec:
  ports:
  - port: 8080
    targetPort: 8080
  selector:
    app: hello-v2
```

## Apply changes

```$bash
kubectl apply -f clusterip.yaml
```

## Display app in the browser after change de service

```$bash
kubectl port-forward service/svc-front 8080:8080
```

## Delete deployment v1

```$bash
kubectl delete -f hello-dep-v1.yaml
```

## Delete service clusterip

```$bash
kubectl delete -f clusterip.yaml
```

## Delete deployment v2

```$bash
kubectl delete -f hello-dep-v2.yaml
```
