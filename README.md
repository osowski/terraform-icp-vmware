# Terraform ICP VMware

This Terraform example configurations uses the [VMware vSphere provider](https://www.terraform.io/docs/providers/vsphere/index.html) to provision virtual machines on VMware
and [TerraForm Module ICP Deploy](https://github.com/ibm-cloud-architecture/terraform-module-icp-deploy) to prepare VMs and deploy [IBM Cloud Private](https://www.ibm.com/cloud-computing/products/ibm-cloud-private/) on them.


### Pre-requisits

* Working copy of [Terraform](https://www.terraform.io/intro/getting-started/install.html)
* The example assumes the VMs are provisioned from a template that has ssh keys loaded in /root/.ssh/authorized_keys
   After VM creation terraform will SSH into the VM to prepare and start installation of ICP using the SSH key provided
* The template is tested on vm templates based on Ubuntu 16.04

### Using the templates

1. git clone or download the templates
1. Navigate to the most relevant example you want to utilise in the [examples](examples) directory 
1. Update the [variables.tf](variables.tf) file to reflect your environment
1. Run `terraform init` to download depenencies (modules and plugins)
1. Run `terraform plan` to investigate deployment plan
1. Run `terraform apply` to start deployment



