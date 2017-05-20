## Prerequisite
### Setup environment values
```sh
export NAME=tower.apiway.io
export KOPS_STATE_STORE=s3://tower-apiway-io-state-store
export KOPS_STATE_S3_ACL=bucket-owner-full-control
export AWS_SECRET_ACCESS_KEY=xxxxx
export AWS_ACCESS_KEY_ID=xxxxxx
```


## Creating apiway-api service
```sh
kubectl create -f apiway-api-service.yaml
```

## Creating apiway-api controller
```sh
kubectl create -f apiway-api-controller.yaml
```



### Node.js and MongoDB on Kubernetes
   
https://github.com/kubernetes/kubernetes/tree/master/examples/nodesjs-mongodb

https://kubernetes.io/docs/getting-started-guides/meanstack/


### Creating the MongoDB Service
To start the service, run:

```sh
kubectl create -f mongo-service.yaml
```

### Creating the MongoDB StatefulSet
```sh
kubectl create -f mongo-statefulset.yaml
```

### Connecting to the MongoDB Service
Connection string URI:
```sh
mongodb://mongo-0.mongo,mongo-1.mongo,mongo-2.mongo:27017/dbname_?
```

### Accessing to Pod with shell
```sh
kubectl exec -it {Pod Name} sh
```

### Exposing mongodb service
```sh
kubectl expose service mongo --type=LoadBalancer --name=mongo-service
```


### References
#### Running MongoDB on Kubernetes with StatefulSets
- http://blog.kubernetes.io/2017/01/running-mongodb-on-kubernetes-with-statefulsets.html
### Running MongoDB as a Microservice with Docker and Kubernetes
- https://www.mongodb.com/blog/post/running-mongodb-as-a-microservice-with-docker-and-kubernetes
#### MEAN stack on Google Cloud Platform:
- https://kubernetes.io/docs/getting-started-guides/meanstack/