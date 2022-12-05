# Microk8s

#### Create a new Ubuntu VM
```
multipass launch --name microk8s --mem 8G
```

#### Install microk8s in the VM
```
multipass exec microk8s -- sudo snap install microk8s --classic
```

#### copy the cluster configuration
```
multipass exec microk8s -- sudo microk8s.config > /tmp/microk8s.yaml
```

#### export the configurations
```
export KUBECONFIG=/tmp/microk8s.yaml
```

#### Inspect the nodes
```
kubectl get nodes
```
