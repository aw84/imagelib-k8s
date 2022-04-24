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
kubectl create configmap configserver-config-map --from-env-file=envs/config-server.env
kubectl create configmap generic-config-map --from-env-file=envs/generic.env
kubectl create configmap api-config-map --from-env-file=envs/api.env

kubectl get cm configserver-config-map -o yaml
kubectl get cm generic-config-map -o yaml
kubectl get cm api-config-map -o yaml
```
# Envs


# Config Service

# Eureka Service

