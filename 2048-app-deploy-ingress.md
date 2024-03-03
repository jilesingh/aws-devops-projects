# Create Fargate profile:
eksctl create fargateprofile \
    --cluster demo-cluster \
    --region eu-central-1 \
    --name alb-sample-sapp \
    --namespace game-2048

## Create Namespace, Deployment, Service and Ingress using the YAML file
kubectl apply -f https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.5.4/docs/examples/2048/2048_full.yaml