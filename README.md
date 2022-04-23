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
setting up `ConfigMap` and `Secrets`
```bash
kubectl create configmap configserver-config-map --from-env-file=config-server.env
kubectl create configmap generic-config-map --from-env-file=generic.env

kubectl get cm configserver-config-map -o yaml
kubectl get cm generic-config-map -o yaml
```
# Config Service

# Eureka Service

