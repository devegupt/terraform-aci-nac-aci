<!-- BEGIN_TF_DOCS -->
# Terraform ACI Application Profile Module

Manages ACI Application Profile

Location in GUI:
`Tenants` » `XXX` » `Application Profiles`

## Examples

```hcl
module "aci_application_profile" {
  source  = "netascode/nac-aci/aci//modules/terraform-aci-application-profile"
  version = ">= 0.8.0"

  tenant      = "ABC"
  name        = "AP1"
  alias       = "AP1-ALIAS"
  description = "My Description"
}
```

## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0.0 |
| <a name="requirement_aci"></a> [aci](#requirement\_aci) | >= 2.0.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aci"></a> [aci](#provider\_aci) | >= 2.0.0 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_tenant"></a> [tenant](#input\_tenant) | Tenant name. | `string` | n/a | yes |
| <a name="input_name"></a> [name](#input\_name) | Application profile name. | `string` | n/a | yes |
| <a name="input_annotation"></a> [annotation](#input\_annotation) | Annotation value. | `string` | `null` | no |
| <a name="input_alias"></a> [alias](#input\_alias) | Application profile alias. | `string` | `""` | no |
| <a name="input_description"></a> [description](#input\_description) | Application profile description. | `string` | `""` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_dn"></a> [dn](#output\_dn) | Distinguished name of `fvAp` object. |
| <a name="output_name"></a> [name](#output\_name) | Application profile name. |

## Resources

| Name | Type |
|------|------|
| [aci_rest_managed.fvAp](https://registry.terraform.io/providers/CiscoDevNet/aci/latest/docs/resources/rest_managed) | resource |
<!-- END_TF_DOCS -->