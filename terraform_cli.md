#             Terraform cheat sheet with commonly used commands and concepts:

## Initialization:

 Initialize a Terraform working directory (downloads providers and modules):
 
  terraform init
 
Configuration:

 ## Validate the Terraform configuration files:
 
  terraform validate
 
 ## Preview the changes that will be made:
 
  terraform plan
 
 ## Apply the changes to create or modify infrastructure:
 
  terraform apply
 
 ## Destroy the created infrastructure:
 
  terraform destroy
 
State Management:
 ## Show the current state of the Terraform-managed infrastructure:
 
  terraform show
 
 ## Refresh the Terraform state against real resources:
 
  terraform refresh
 
 ## Manually manipulate the Terraform state:
 
  terraform state <subcommand>
 
Workspace Management:
 ## List available workspaces:
 
  terraform workspace list
 
 ## Create a new workspace:
 
  terraform workspace new <workspace-name>
 

 ## Select an existing workspace:
 
  terraform workspace select <workspace-name>
 
 ## Delete a workspace:
 
  terraform workspace delete <workspace-name>
 
Module Usage:
 ## Download and update modules required for the configuration:
 
  terraform get -update=true
 
 ## Initialize a module in a Terraform working directory:
 
  terraform init -from-module=<module-source>
 
Input Variables:
 ## Define input variables (values provided externally):
 
  variable "<var-name>" {
    description = "<description>"
    type        = <type>
    default     = <default-value>
  }
 
 ## Provide input variable values via a file:
 
  terraform apply -var-file=<var-file>
 
Output Values:
 ## Define output values to display after applying changes:
 
  output "<output-name>" {
    value = <expression>
  }

 ##Show the output values after applying changes:
 
  terraform output
 
 ## Remote State: 

 ## Configure a backend to store the Terraform state remotely:
 
  terraform {
    backend "<backend-name>" {
      // backend configuration
    }
  }
 
 ## Initialize a new backend for remote state storage:
 
 terraform init -backend-config=<config-file>
 
## Working with workspaces
terraform workspace new dev
terraform workspace new stage
terraform workspace new prod

## To switch between workspaces
terraform workspace select dev
terraform workspace select stage
terraform workspace select prod

 
 ## Notes:
 
 For more details and advanced usage, refer to the Terraform documentation at https://www.terraform.io/docs/index.html.
