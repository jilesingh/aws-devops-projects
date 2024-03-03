# Install EKS

### Please follow the prequisites doc before this

## Install using Fargate
    eksctl create cluster --name demo-cluster --region eu-central-1 --fargate

## Delete the Cluster
    eksctl delete cluster --name demo-cluster --region eu-central-1
