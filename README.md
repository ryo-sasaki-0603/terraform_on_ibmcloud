# Repo for Terraform on IBM Cloud learning plan

This repository is for the Terraform files created in the following courses of the Terraform on IBM Cloud learning plan.

 - Setting up Terraform for IBM Cloud Container Registry
 - Creating single and multizone Kubernetes and OpenShift clusters
 - Provisioning an IBM Cloud virtual server for VPC

## Setting up Terraform for IBM Cloud Container Registry

In main.tf, add configuration to create a container registry namespace and assign IAM to users.
Use the HashiCorp Configuration Language (HCL) to set the access policy for that namespace in Cloud Identity and Access Management (IAM).


cd directory

```bash
$ cd ./ibmcloud_container_registry
```

Initialize the Terraform CLI.

```bash
$ terraform init
```

Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to create the Container Registry namespace and IAM access policy in your account.

```bash
$ terraform plan
```

Create the Container Registry namespace and IAM access policy in IBM Cloud.

```bash
$ terraform apply
```

## Creating single and multizone Kubernetes and OpenShift clusters

Create an IBM Cloud configuration file for a single-zone cluster using Terraform. In main.tf, create a single-zone cluster with a default worker pool in the dal10 zone. This worker pool consists of three worker nodes and connects to both the private VLAN and public VLAN within dal10.

cd directory

```bash
$ cd ./tf-cluster
```

Initialize the Terraform CLI.

```bash
$ terraform init
```

Create an Terraform on IBM Cloud execution plan. When you execute this command, Terraform on IBM Cloud validates the syntax of your configuration file and resource definitions against the specifications of the IBM Cloud Provider plug-in.

```bash
$ terraform plan
```

Create your single zone cluster. Note that the creation of your cluster takes a few minutes to complete.

```bash
$ terraform apply
```


## Provisioning an IBM Cloud virtual server for VPC

Create the following resources in vpc.tf:

 - VPC where you provision your VPC virtual server instance
 - security group and a rule for this security group to allow SSH connection to your virtual server instance
 - subnet to enable networking in your VPC
 - VPC virtual server instance
 - floating IP address that you use to access your VPC virtual server instance over the public network

cd directory

```bash
$ cd ./ibmcloud_vs_for_vpc
```

Initialize the Terraform CLI.

```bash
$ terraform init
```

Generate an Terraform on IBM Cloud execution plan. When you execute this command, Terraform on IBM Cloud validates the syntax of your configuration file and resource definitions against the specifications that are provided by the IBM Cloud Provider plug-in.

```bash
$ terraform plan
```

Create the VPC infrastructure resources. Confirm the creation by entering yes when prompted.

```bash
$ terraform apply
```