# aks-cluster-terraform

Terraform files for provision the AKS cluster.

## Setup

### Terraform init and setup

    terraform init
    terraform apply

### Configure kubectl

    az aks get-credentials --resource-group $(terraform output resource_group_name) --name $(terraform output kubernetes_cluster_name)

### Access Kubernetes Dashboard

    kubectl create clusterrolebinding kubernetes-dashboard --clusterrole=cluster-admin --serviceaccount=kube-system:kubernetes-dashboard
