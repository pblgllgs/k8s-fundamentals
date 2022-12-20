# Statefulset

## Create a Statefulset

```$bash
kubectl apply -f statefulset.yaml
```

## Get pod list

```$bash
kubectl get pods -o wide
```

## Get pod persistent volumes

```$bash
kubectl get pvc
```

## create a file in third pod

```$bash
kubectl exec -it nginx-sts-2 -- /bin/sh
# cd /var/www
# pwd
/var/www
# echo Hello > hello.txt
```

## Modify the default web page

```$bash
# cd /usr/share/nginx/html
# pwd
/usr/share/nginx/html
# cat > index.html
Hello
Ctrl-D
# cat index.html
Hello
# exit
```

## Open the first pod

```$bash
kubectl exec -it nginx-sts-0 -- /bin/sh
# curl http://nginx-sts-2.nginx-headless
# exit
```

## Delete third pod

```$bash
kubectl delete pod nginx-sts-2
kubectl exec -it nginx-sts-2 -- /bin/sh
ls /var/www
cat /var/www/hello.txt
```

## Delete statefulset and persistent volumes

```$bash
kubectl delete -f statefulset.yaml
kubectl delete pvc www-nginx-sts-0
kubectl delete pvc www-nginx-sts-1
kubectl delete pvc www-nginx-sts-2
```
