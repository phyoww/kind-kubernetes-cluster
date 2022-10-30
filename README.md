# Kubernets running on kind cluster with Manifests
# Pre-requisites
### brew install kubectl
### brew install kind
### brew install helm
### install docker desktop

# Step:
## 1.Configuring a KIND cluster (kind: Cluster)/Kubernetes and that the version of KIND's config we are using is v1alpha4 (apiVersion: kind.x-k8s.io/v1alpha4).

[Uploading config.yaml…]()


# Run the below command to create kubernetes cluster
```bash
kind create cluster --name my-kube-cluster --config config.yaml
```

<img width="980" alt="kind" src="https://user-images.githubusercontent.com/85800387/198857848-ff0a0996-e16b-494f-aba0-d55318f5cd52.png">


# 2.Verify kubernetes nodes on kind cluster

```bash
docker images | grep kind
kubectl get nodes
kubectl get ns
kubectl get nodes -o wide
```


<img width="1288" alt="nodes" src="https://user-images.githubusercontent.com/85800387/198857861-d401e7a2-0f16-4400-bfbf-d73882997164.png">


<img width="789" alt="svc" src="https://user-images.githubusercontent.com/85800387/198857866-5e2b6df6-0033-412a-b847-2965df238778.png">


<img width="547" alt="namespace" src="https://user-images.githubusercontent.com/85800387/198857876-afc5bbc5-714b-4554-abc3-3bf965a3ec3a.png">


<img width="1265" alt="docker" src="https://user-images.githubusercontent.com/85800387/198857878-fdf99840-b568-4c46-aa63-2a348cbc3595.png">



#### 3.Create metallb.yaml file (TBC)
#### 4.Install metallb by Manifest (TBC)



# 5.Delete the kind cluster.


```bash
kind delete cluster --name my-kube-cluster
```
<img width="750" alt="deletecluster" src="https://user-images.githubusercontent.com/85800387/198857887-a1322056-a44e-43bc-9051-7cbc8e9156a6.png">

