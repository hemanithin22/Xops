# XOps Task 5 – Kubernetes with kind

## Objective

Deploy a local Kubernetes cluster with kind and serve a custom NGINX page.

## Screenshot

![Kubernetes Dashboard Screenshot](Screenshots/webpage.png)

## Project Structure

```
/kubernetes-xops-task5
├── README.md
├── index.html
├── app.yaml
├── screenshots/
```

## Steps

1. **Create Cluster**

```powershell
kind create cluster --name xops-cluster
kubectl get nodes
```

2. **Create ConfigMap**

```powershell
kubectl create configmap xops-web-content --from-file=index.html
```

3. **Deploy App**

```powershell
kubectl apply -f app.yaml
kubectl get pods,svc
```

4. **Access App**

```powershell
kubectl port-forward deployment/xops-web 8080:80
```

Visit: `http://localhost:8080`

## Kubernetes Components

* **API Server**: Handles REST requests.
* **Scheduler**: Assigns Pods to nodes.
* **Controller Manager**: Maintains cluster state.
* **etcd**: Key-value cluster store.
* **kubelet**: Node agent managing Pods.
* **kube-proxy**: Handles networking and service routing.

## Clean Up

```powershell
kind delete cluster --name xops-cluster
```
