DOCKER
start all docker containers:
docker compose up -d
URL: http://localhost:3000

Minikube:
minikube start
kubectl config use-context minikube
minikube service frontend-service

Grafana:
kubectl port-forward -n monitoring service/monitoring-grafana 3001:80
URL: http://localhost:3001
username: admin
password: fnKKunqocbmwT9SGLvf5Fr8xRGmkw1pIeIdGRCnZ

OpenFaaS:
kubectl get pods -n openfaas
kubectl port-forward -n openfaas svc/gateway 8080:8080
URL: http://localhost:8080
username: admin
password: hgIgtBDqSQZIXW5yuGcXaPOuFe88o7TV

K3s cluster:
k3d cluster start edge-cluster
