# wordpress-kubernetes

## Start
```
$ minikube start
$ kubectl apply -f mysql-pass.yml
$ kubectl apply -f mysql-deployment.yml
$ kubectl apply -f wordpress-deployment.yml
```

## Access
```
$ minikube service wordpress
```

## Delete
```
$ kubectl delete -f mysql-pass.yml
$ kubectl delete -f mysql-deployment.yml
$ kubectl delete -f wordpress-deployment.yml
$ minikube stop
```

## Deploy to GCP
```
$ gcloud components install kubectl
$ gcloud projects create --name wordpress-kubernetes
$ gcloud config set $PROJECT_ID
$ gcloud container clusters create wordpress-kubernetes --num-nodes=2 \
--zone asia-northeast1-a \
--machine-type g1-small \
--enable-autoscaling --min-nodes=2 --max-nodes=5

```

## Ref
* [Example: Deploying WordPress and MySQL with Persistent Volumes](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)
