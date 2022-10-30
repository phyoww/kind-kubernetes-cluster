# Kubernets running on kind cluster with Manifests
# Pre-requisites
### brew install kubectl
### brew install kind
### brew install helm
### install docker desktop

# Step:
## 1.Configuring a KIND cluster (kind: Cluster)/Kubernetes and that the version of KIND's config we are using is v1alpha4 (apiVersion: kind.x-k8s.io/v1alpha4).

- [config.yaml](config.yaml)

# Run the below command to create kubernetes cluster
```bash
kind create cluster --name my-kube-cluster --config config.yaml
```

![Kind](photo/kind.png)

# 2.Verify kubernetes nodes on kind cluster

```bash
docker images | grep kind
kubectl get nodes
kubectl get ns
kubectl get nodes -o wide
```

![header image](photo/nodes.png)

![header image](../photo/svc.png)

![header image](/photo/namespace.png)

![header image](/photo/docker.png)

#### 3.Create metallb.yaml file (TBC)
#### 4.Install metallb by Manifest (TBC)



# 5.Delete the kind cluster.


```bash
kind delete cluster --name my-kube-cluster
```

![header image](/photo/deletecluster.png)
