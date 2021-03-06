<!-- BEGIN_TF_DOCS -->
# azuredevops_repositories

This module manages Azure DevOps Repositories.

<-- This file is autogenerated, please do not change. -->

## Requirements

| Name | Version |
|------|---------|
| terraform | ~> 1.2.0 |
| azuredevops | =0.2.1 |

## Providers

| Name | Version |
|------|---------|
| azuredevops | =0.2.1 |

## Resources

| Name | Type |
|------|------|
| azuredevops_git_repository.git_repository | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| git_repository | resource definition, default settings are defined within locals and merged with var settings | `any` | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| git_repository | azuredevops_git_repository results |

## Examples

```hcl
module "repositories" {
  source = "registry.terraform.io/T-Systems-MMS/pipelines/repositories"
  git_repository = {
    azuredevops = {
      project_id = module.project.project["project_name"].id
    }
  }
}
```
<!-- END_TF_DOCS -->
