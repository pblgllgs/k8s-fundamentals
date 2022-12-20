# Job

## Create a job

```$bash
kubectl apply -f job.yaml
```

## Get all jobs

```$bash
kubectl get jobs
```

## describe job

```$bash
kubectl describe jobs
```

## Get all pods

```$bash
kubectl get pods
```

## View logs of the specific pod

```$bash
kubectl  logs <POD_NAME>
```

## Delete deployment

```$bash
kubectl delete -f job.yaml
```
