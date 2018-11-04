# wordpress-kubernetes

## Start
```
$ minikube start
$ kubectl apply -f mysql-pass.yml
$ kubectl apply -f mysql-deployment.yaml
$ kubectl apply -f wordpress-deployment.yml
```

## Access
```
$ minikube service wordpress
```

## Delete
```
$ kubectl delete -f mysql-pass.yml
$ kubectl delete -f mysql-deployment.yaml
$ kubectl delete -f wordpress-deployment.yml
$ minikube stop
```

## Ref
* [Example: Deploying WordPress and MySQL with Persistent Volumes](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)
