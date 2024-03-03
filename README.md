# aws-devops-projects

1. Install kubectl on your local machine: https://kubernetes.io/docs/tasks/tools/
2. Install eksctl: https://eksctl.io/installation/#
3. Install AWS CLI: https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
4. Create a EKS cluster: eksctl create cluster --name demo-cluster --region eu-central-1 --fargate
5. Configure OIDC Connector using [configure-oidc-connectore.md](configure-oidc-connectore.md) 
6. Install Helm: https://helm.sh/docs/intro/install/
7. Finally set-up and deploy alb-controller-add-on using [alb-controller-add-on.md](alb-controller-add-on.md)

# Error encounters because serviceAccount was already existed so to override if it is the case 
    eksctl create iamserviceaccount   --cluster=demo-cluster   --namespace=kube-system   --name=aws-load-balancer-controller   --role-name AmazonEKSLoadBalancerControllerRole   --attach-policy-arn=arn:aws:iam::AKIAW4YHIRXCLG4LGOM6/AWSLoadBalancerControllerIAMPolicy   --approve --override-existing-serviceaccounts

    eksctl create iamserviceaccount   --cluster=demo-cluster   --namespace=kube-system   --name=aws-load-balancer-controller-1   --role-name AmazonEKSLoadBalancerControllerRole   --attach-policy-arn=arn:aws:iam::AKIAW4YHIRXCLG4LGOM6/AWSLoadBalancerControllerIAMPolicy   --approve --override-existing-serviceaccounts