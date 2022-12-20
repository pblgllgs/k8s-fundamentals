# CronJob

## Create a cronjob

```$bash
kubectl apply -f cronjob.yaml
```

## Get all jobs

```$bash
kubectl get cronjobs
```

## describe job

```$bash
kubectl describe cronjobs
```

## Get all pods

```$bash
kubectl get pods
```

## View logs of the specific pod

```$bash
kubectl logs <POD_NAME>
```

## Delete deployment

```$bash
kubectl delete -f cronjob.yaml
```
