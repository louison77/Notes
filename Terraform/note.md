# Terraform

---

## Principles

---

* IAC (Infradtructure As Code) tool
* Manage easily infrastructure: On premise or Cloud ( AWS, GCP, Azure, ...)
* It is Open source and developped by Hashicorp in Go language
* A lot of different providers available( check the Terraform's website)
* Use state files to check the state of the resources
* Declare infrastructure code in .tf files.

## Main commands

---

Terraform is a command line tool. The main commands used to manage the resources are:

1. `terraform init` : It is the command that allows to initialize the terraform repository. Actually this command import the required provider to execute the code.
2. `terraform plan` : It shows the resources that will be created, modified and destroy when applying the plan.
3. `terraform apply` : It apply the plan. Use the *-auto-approve* flag to skip the manual validation.
4. `terraform show` : Show metadata of the created resources.
5. `terraform get` : Import the required terraform's modules.
6. `terraform destroy` : Destroy the resources described in the plan.

## Good practices and tips

* Terraform files can be described as modules. In the root, at the root of the project, a folder "modules" needs to be created.
* Separate the outputs, variables and resources in different files. Ex: outputs.tf, variables.tf, terraform.tfvars, main.tf, ....
* It exists different variable's levels depending when they are declared. 1 - Defined as TF_VAR_name as environment variable 2 - Defined in the terraform.tfvars file 3 - In the file terraform.tfvarrs.json 4 - In a file *.auto.tfvars(.json) 5 - With the CLI command apply and the flag -var or - var-file. (Don't forget quotes)
* Check the documentation of every terraform object in the websites. They are mandatory parameter to create a resource and other that are mandatory depending of the will.
