
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


### Kubernetes Doc - References:
- [ConfigMaps](https://kubernetes.io/docs/concepts/configuration/configmap/)
- [Secrets](https://kubernetes.io/docs/concepts/configuration/secret/)
- [Deployments](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
- [Service](https://kubernetes.io/docs/concepts/services-networking/service/)