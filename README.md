# tf-move-state
tf-move-state
Start with 1 folder with multiple state, end with 2 folder, separate state and module.

1 - Create 1 folder for sample code, run terraform apply *
2 - Create a folder for random_pet
    Make code for a module
3 - Update code to use module
     Terraform init
     Use terraform state mv to rename the state
4 - Terraform apply should say the nothing to be created, state should persists.
5 - Terraform destroy should work and delete the existing state
