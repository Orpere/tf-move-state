# tf-move-state

  
- [x] git clone and move to the directory tf-move-state
  
```bash
git@github.com:orlando-pereira/tf-move-state.git
```

- [x] run terraform init and apply
  
```bash
cd sample
terraform init
terraform apply
cd ../random
terraform init
```

- [x] Use terraform state mv to rename the state
  
```bash
cd sample
terraform state mv -state-out=../random/terraform.tfstate null_resource.hello null_resource.hello
terraform state mv -state-out=../random/terraform.tfstate random_pet.name random_pet.name
```

- [x] Terraform apply should say the nothing to be created, state should persists.

```bash
terraform apply
null_resource.hello: Refreshing state... [id=8265997636075935698]
random_pet.name: Refreshing state... [id=verbally-adversely-honest-tortoise]
```

- [x] Terraform destroy should work and delete the existing state

```bash
terraform destroy
```

```bash
null_resource.hello: Destroying... [id=8265997636075935698]
null_resource.hello: Destruction complete after 0s
random_pet.name: Destroying... [id=verbally-adversely-honest-tortoise]
random_pet.name: Destruction complete after 0s

Destroy complete! Resources: 2 destroyed.
```
