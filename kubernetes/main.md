# Kubernetes

### kubectl Cheat Sheet
```
kubectl get pods
kubectl get pods -n kube-system
kubectl get pods <pod-name> -o jsonpath='{.spec.containers[*].name}{"\n"}'
kubectl get nodes
kubectl get nodes -o wide

kubectl get services
kubectl get service --all-namespaces
kubectl get ep

kubectl logs -f <pod-name> --tail 200
kubectl logs -f <pod-name> --tail 200 -c <container-name>

kubectl ctreate -f <manifest.yaml>
kubectl describe pods <pod-name>


kubectl proxy
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0/aio/deploy/recommended.yaml
kubectl get secrets
kubectl describe secret dashboard-admin-sa-token-kw7vn
```

### Change Context
```
kubectl config get-contexts
kubectl config current-context
kubectl config set-context docker-desktop
```

- [The Ultimate Guide to the Kubernetes Dashboard: How to Install, Access, Authenticate and Add Heapster Metrics](https://www.replex.io/blog/how-to-install-access-and-add-heapster-metrics-to-the-kubernetes-dashboard)


### Components
```
+ Pod
+ ReplicaSet
HorisontalScaling
Deployment
Service
    ClusterIP
    NodePort
    LoadBalancer
    ExternalName
StatefulSet
Job
CronJob
Ingress
ConfigMap
Secret
```

# Tools
- [A Multitude of Kubernetes Deployment Tools: Kubespray, kops, and kubeadm](https://www.altoros.com/blog/a-multitude-of-kubernetes-deployment-tools-kubespray-kops-and-kubeadm/)


# Github
- [kelseyhightower/kubernetes-the-hard-way](https://github.com/kelseyhightower/kubernetes-the-hard-way)