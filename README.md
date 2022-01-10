# Repository for learning Terraform

## This Repository creates an AWS instance with Terraform CLI

## Instructions

### Prerequisites
- [X] [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

- [X] [Vagrant](https://www.vagrantup.com/downloads)

- [X] [Terraform](https://www.terraform.io/downloads)


## How to Use this Repo

- Clone this repository:
```shell
git clone git@github.com:dlavric/terraform-aws.git
```

- Go to the directory where the repo is stored:
```shell
cd terraform-aws
```


- Start Vagrant
```shell
vagrant up
```

- Connect to the VM
```
vagrant ssh terraform
```

- Configure your own AWS and introduce your Access Key ID and the Secret Key
```
aws configure
```

- Go to the directory where the `main.tf` file is located
```
cd /vagrant/learn-terraform-aws-instance
```

- Initialize Terraform and apply the changes
```
terraform init
terraform plan
terraform apply
```


- Destroy the Vagrant machine:
```shell
vagrant destroy
```

