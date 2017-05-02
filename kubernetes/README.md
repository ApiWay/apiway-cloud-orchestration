### Node.js and MongoDB on Kubernetes
   
https://github.com/kubernetes/kubernetes/tree/master/examples/nodesjs-mongodb

https://kubernetes.io/docs/getting-started-guides/meanstack/

```sh
export NAME=tower.apiway.io
export KOPS_STATE_STORE=s3://tower-apiway-io-state-store
export KOPS_STATE_S3_ACL=bucket-owner-full-control
export AWS_SECRET_ACCESS_KEY=xxxxx
export AWS_ACCESS_KEY_ID=xxxxxx
```

### Creating the MongoDB Service
To start the service, run:

```sh
kubectl create -f mongo-service.yaml
```

### Creating the MongoDB StatefulSet
```sh
kubectl create -f mongo-statefulset.yaml
```

### References
#### Running MongoDB on Kubernetes with StatefulSets
- http://blog.kubernetes.io/2017/01/running-mongodb-on-kubernetes-with-statefulsets.html
#### MEAN stack on Google Cloud Platform:
- https://kubernetes.io/docs/getting-started-guides/meanstack/