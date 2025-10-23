
## Resources
- [Kubernetes Crash Course for Absolute Beginners](https://youtu.be/s_o8dwzRlu4?si=S0tQ1CRqGuDYw87A)
- [Kubernetes offical docs](https://kubernetes.io/docs/home/)

### Explanation
It has 4 config files
- ConfigMap
    - MongoDB Endpoint
- Secret
    - MongoDB User & Pwd
- Deployment service
    - MongoDb App with internal service
- Deployment Service
    - Our own WebApp with external service

### Run

``` bash
kubectl apply -f mongo-config.yaml
```
- respone: configmap/mongo-config created
``` bash
kubectl apply -f mongo-secret.yaml
```
- response: secret/mongo-secret created
``` bash
- kubectl apply -f mongo.yaml
```
- response:
    - deployment.apps/mongo-deployment created
    - service/mongo-service created

``` bash
kubectl get all
```
- returns all the Components created in Cluster

``` bash
kubectl get svc
```
- svc = service


``` bash
kubectl get node -o wide
minikube ip
```
- To get the ip of the minikube



### Commonly usted k8s commands


``` bash
kubectl get pod
```
``` bash
kubectl get configmap
```
``` bash
kubectl get secret
```
``` bash
kubectl --help
```
``` bash
kubectl get --help
```

``` bash
kubectl describe service webpp-service
```
- Gives more detailed output of the specific component!

``` bash
kubectl describe pod <POD_NAME>
```
- Gives more detailed about POD!

``` bash
kubectl log <POD_NAME>
```
- Gives logs of the container inside the POD

``` bash
kubectl log <POD_NAME> -f
```
- Stream the logs of the container inside the POD


### Explanation
- apply manages applications through files defining K8s resources (-f stands for file)

### Kubernetes Doc - References:
- [ConfigMaps](https://kubernetes.io/docs/concepts/configuration/configmap/)
- [Secrets](https://kubernetes.io/docs/concepts/configuration/secret/)
- [Deployments](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
- [Service](https://kubernetes.io/docs/concepts/services-networking/service/)