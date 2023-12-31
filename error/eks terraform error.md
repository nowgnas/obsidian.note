```shell
Error: Missing required argument
│ 
│   with helm_release.release,
│   on loadbalancer.tf line 48, in resource "helm_release" "release":
│   48: resource "helm_release" "release" {
│ 
│ The argument "set.0.value" is required, but no definition was found.
╵
╷
│ Error: waiting for EC2 NAT Gateway (nat-0283dec33a15eeb58) create: RequestError: send request failed
│ caused by: Post "https://ec2.ap-northeast-2.amazonaws.com/": read tcp [2001:2d8:e51a:f416:4188:1628:ed4f:1815]:50050->[64:ff9b::345f:c143]:443: read: connection reset by peer
│ 
│   with module.vpc.aws_nat_gateway.this[0],
│   on .terraform/modules/vpc/main.tf line 1059, in resource "aws_nat_gateway" "this":
│ 1059: resource "aws_nat_gateway" "this" {
│ 
╵
╷
│ Error: waiting for EKS Node Group (bb-test:service2-20231231055334847500000020) create: unexpected state 'CREATE_FAILED', wanted target 'ACTIVE'. last error: i-0e851de4ac57a0a68: NodeCreationFailure: Instances failed to join the kubernetes cluster
│ 
│   with module.eks.module.eks_managed_node_group["service2"].aws_eks_node_group.this[0],
│   on .terraform/modules/eks/modules/eks-managed-node-group/main.tf line 308, in resource "aws_eks_node_group" "this":
│  308: resource "aws_eks_node_group" "this" {
│ 
╵
╷
│ Error: waiting for EKS Node Group (bb-test:service1-2023123105533484740000001e) create: unexpected state 'CREATE_FAILED', wanted target 'ACTIVE'. last error: i-00e594c4bd7a00b77: NodeCreationFailure: Instances failed to join the kubernetes cluster
│ 
│   with module.eks.module.eks_managed_node_group["service1"].aws_eks_node_group.this[0],
│   on .terraform/modules/eks/modules/eks-managed-node-group/main.tf line 308, in resource "aws_eks_node_group" "this":
│  308: resource "aws_eks_node_group" "this" {
│ 
╵
╷
│ Error: waiting for EKS Node Group (bb-test:service3-2023123105533484740000001d) create: unexpected state 'CREATE_FAILED', wanted target 'ACTIVE'. last error: i-0d2ede8561182a359: NodeCreationFailure: Instances failed to join the kubernetes cluster
│ 
│   with module.eks.module.eks_managed_node_group["service3"].aws_eks_node_group.this[0],
│   on .terraform/modules/eks/modules/eks-managed-node-group/main.tf line 308, in resource "aws_eks_node_group" "this":
│  308: resource "aws_eks_node_group" "this" {

```
https://devblog.kakaostyle.com/ko/2022-03-31-3-build-eks-cluster-with-terraform/