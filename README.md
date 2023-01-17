# Observability cluster
Using Terraform to install the Fluxcd manifests in a Kubernetes Cluster which will, then, install everything from the Git Repository in a GitOps approach.

# Requisites
- Having a local Kubernetes Cluster running (if you're going for a remote one, then the terraform code needs to be adjusted)
- Having Terraform CLI installed

# Getting started
Since we're using Terraform to install the Flux manifests and are relaying on GitOps to do the rest, we just need to apply the Terraform code.
To be able to do that, we need to provide Fluxcd with a Token to access the Git repository it should track (i.e. for GitHub, you can create a Personal Access Token).

``` bash
cd terraform/
terraform init
terraform apply -var=<flux-token>
```


