# Minikube-Helm-Prometheus-and-Grafana-
mention by AB | Simplified Kubernetes Monitoring with Minikube, Helm, Prometheus, and Grafana
![Simplified Kubernetes Monitoring with Minikube, Helm, Prometheus, and Grafana](https://media.licdn.com/dms/image/D4D12AQFAWnVwEVNGsw/article-cover_image-shrink_720_1280/0/1718920229402?e=1724284800&v=beta&t=0_l7rynPQIvGNJIzBlmZwejdDDt3B7m33mwDcdT_egU)


```
sudo su
```
# Update apt package index and install Docker
```
sudo apt update && apt -y install docker.io
```
# Install kubectl
```
curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl && chmod +x ./kubectl && sudo mv ./kubectl /usr/local/bin/kubectl
```
# Install Minikube
```
curl -Lo minikube https://github.com/kubernetes/minikube/releases/download/v1.24.0/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
```
# Install conntrack (dependency for Minikube)
```
apt install conntrack
```
# Install crictl (optional, for container runtime inspection)
```
wget https://github.com/kubernetes-sigs/cri-tools/releases/download/v1.22.0/crictl-v1.22.0-linux-amd64.tar.gz
```
```
tar -zxvf crictl-v1.22.0-linux-amd64.tar.gz
sudo mv crictl /usr/local/bin/
crictl --version
```

2. Start Minikube:
```
minikube start --vm-driver=none
minikube status
```

## Step 2: Install Helm
```
curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash
```












































































