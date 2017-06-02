![logo](https://github.com/ApiWay/apiway-design/blob/master/img/logo.png)

# ApiWay: Container Orchestration using Kubernetes
Automating deployment, scaling, and management of containerized applications for apiway.io

### Main Feature
* Auto scaling
* Load balancing & Service discovery
* Self-healing
* Automated rollouts and rollbacks
* Storage orchestration

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
### Creating apiway-pubsub service
```sh
kubectl create -f apiway-pubsub-service.yaml
```
### Creating apiway-pubsub deployment
```sh
kubectl create -f apiway-pubsub-deployment.yaml
```
### Creating apiway-smtp service
```sh
kubectl create -f apiway-smtp-service.yaml
```
### Creating apiway-smtp deployment
```sh
kubectl create -f apiway-smtp-deployment.yaml

### References
#### Running MongoDB on Kubernetes with StatefulSets
- http://blog.kubernetes.io/2017/01/running-mongodb-on-kubernetes-with-statefulsets.html
### Running MongoDB as a Microservice with Docker and Kubernetes
- https://www.mongodb.com/blog/post/running-mongodb-as-a-microservice-with-docker-and-kubernetes
#### MEAN stack on Google Cloud Platform:
- https://kubernetes.io/docs/getting-started-guides/meanstack/


![ApiWay Tech. Stack](https://github.com/ApiWay/apiway-cli/blob/master/docs/img/apiway_tech_stack.png)


## Related Projects
#### Web App
* [apiway-web](https://github.com/ApiWay/apiway-web)
#### CLI
* [apiway-cli](https://github.com/ApiWay/apiway-cli)
#### API
* [apiway-api](https://github.com/ApiWay/apiway-api)
#### SDK
##### Javascript
* [apiway-sdk-js](https://github.com/ApiWay/apiway-sdk-js)
* [npm: apiway.js](https://www.npmjs.com/package/apiway.js)
#### Job
* [apiway-job](https://github.com/ApiWay/apiway-job)
#### Design
* [apiway-design](https://github.com/ApiWay/apiway-design)
