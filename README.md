# CI-CD-app-deployment-with-AWS
Group project with continuous integration and deployment on AWS for a web shopping service

# Group #
* Hayet Yefsah ->
[hayetyefsah](https://github.com/hayetyefsah)
* Arnaud Dejeammes ->
[Arnaud-Dejeammes](https://github.com/Arnaud-Dejeammes)
* Charles Ramade ->
[Smogg22](https://github.com/Smogg22)

# Description #

From a git repository of an app divided in micro-services:
https://gitlab.com/ma.it.consulting/projet-fil-rouge-neosoft.git

We created one AWS CodeCommit (github repository) each in order to create pipeline for continuous integration and development.
As soon as we commit and push modifications to one of our micro-services,a new image is automatically generated thanks to a buildspec.yaml file.

Then we deployed an infrastructure thanks to AWS CloudFormation. In this infra, there are:
- 1 Virtual Private Cloud
- 2 Public Subnets
- 2 Security Group
- 1 Internet Gateway
- 1 VPC Gateway Attachment
- 1 Route Table
- 1 Route
- 2 Subnet Route Table Associations
- 1 Role for AWS EKS service
- 1 Role for AWS EKS nodes
- 1 EKS (Kubernetes) cluster
- 1 EKS nodegroup, in which we defined a resource template and auto-scaling policy

Finally, we managed micro-services deployment in nodes thanks to manifest files in yaml format. These manifests also define ports our micro-services use to communicate between them and outside the cluster.
