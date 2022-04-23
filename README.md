# Minikube setup

Setting up Bash environment variables
```bash
eval $(minikube -p minikube docker-env)
```
Starting infrastructure for `LoadBalancer` services
```bash
minikube tunnel
```
Setting up infrastructure for `hostPath` volumes
```bash
minikube mount ~/repos:/hostrepos
```
# Config Service

# Eureka Service

