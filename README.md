# This module creates EKS cluster

### Variables
```
cluster_name                                    = "my-cluster"
cluster_version                                 = "1.15"
subnets                                         = ["subnet-00000", "subnet-00000", "subnet-00000"]
vpc_id                                          = "vpc-0000000000"
instance_type                                   = "m4.large"
asg_max_size                                    = 5
asg_min_size                                    = 1
region                                          = "us-east-2"

```

### Copy and paste below codes if you want to see the outputs

```
output "cluster_id" {
	value = "${module.my-cluster.cluster_id}"
}
output "cluster_arn" {
	value = "${module.my-cluster.cluster_arn}"
}
output "cluster_version" {
	value = "${module.my-cluster.cluster_version}"
}
output "cluster_security_group_id" {
	value = "${module.my-cluster.cluster_security_group_id}"
}
output "workers_asg_names" {
	value = "${module.my-cluster.workers_asg_names}"
}

```

### Run below command
``` 
terraform_0.13.1 init
terraform_0.13.1 plan -var-file regions/ohio.tfvars
terraform_0.13.1 apply -var-file regions/ohio.tfvars

```
