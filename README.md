### Demo Project:

Ansible & Docker

### Technologies used:

Ansible, AWS, Docker, Terraform, Linux

### Project Description:

1- Create AWS EC2 Instance with Terraform

2- Write Ansible Playbook that installs necessary technologies like Docker and Docker Compose, copies docker-compose file to the server

3- Starts the Docker containers configured inside the docker- compose file

### Usage instruction

###### Step 1: Create AWS EC2 Instance with Terraform

1-Create a terraform.tfvars file under the root of the current folder with the following variables

```
vpc_cidr_block =
subnet_cidr_block =
availability_zone =
env_profix =
my_ip_address =
instance_type =
public_key_location  =
```

2-configure aws credentials with specified region and access_id and secret_key

```
cd ec2-instance
```

```
aws configuration
```

3- Initialize the Terraform project

```
terraform init
```

4- Create the VPC and EC2 instance in it

```
terraform apply --auto-approve
```

###### Step 2: Create docker_deploy_app.yaml

#1 Update yum package, install python3 and docker

#2 Install docker-compose

#3 Start docker deamon

#4 Install python docker docker-compose package module

#5 Add ec2-user to docker group and reset connection

#6 Copy docker-compose.yaml file to ec2 server

#7 Docker login

#8 Start app via docker-compose

###### Step 3: Execute the docker_deploy_app.yaml

```
ansible-playbook docker_deploy_app.yaml
```

![image](images/Screenshot%202023-04-21%20at%202.14.36%20pm.png)
