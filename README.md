# Terraform Azure

[![GitHub](https://img.shields.io/github/license/wozorio/terraform-azure-linux-vm)](https://github.com/wozorio/terraform-azure-linux-vm/blob/master/LICENSE)
[![CI](https://github.com/wozorio/terraform-azure-linux-vm/actions/workflows/ci.yml/badge.svg)](https://github.com/wozorio/terraform-azure-linux-vm/actions/workflows/ci.yml)
[![Deploy](https://github.com/wozorio/terraform-azure-linux-vm/actions/workflows/deploy.yml/badge.svg)](https://github.com/wozorio/terraform-azure-linux-vm/actions/workflows/deploy.yml)

Terraform code for deploying a Linux VM with Ubuntu 20.04 LTS (Focal Fossa) in Azure with GitHub Actions.

## Shutdown and Start

To save costs, the virtual machine is shutdown and started every day automatically with respective workflows in GitHub Actions. The shutdown is triggered at 11:00 PM UTC and the startup at 4:00 AM UTC.

<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.15 |
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | 3.67.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | 3.67.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_nsg_vm_ubuntu"></a> [nsg\_vm\_ubuntu](#module\_nsg\_vm\_ubuntu) | ./modules/network_security_group/ | n/a |
| <a name="module_vm_ubuntu"></a> [vm\_ubuntu](#module\_vm\_ubuntu) | ./modules/linux_virtual_machine/ | n/a |

## Resources

| Name | Type |
|------|------|
| [azurerm_network_interface.vm_ubuntu](https://registry.terraform.io/providers/hashicorp/azurerm/3.67.0/docs/resources/network_interface) | resource |
| [azurerm_network_interface_security_group_association.vm_ubuntu](https://registry.terraform.io/providers/hashicorp/azurerm/3.67.0/docs/resources/network_interface_security_group_association) | resource |
| [azurerm_public_ip.vm_ubuntu](https://registry.terraform.io/providers/hashicorp/azurerm/3.67.0/docs/resources/public_ip) | resource |
| [azurerm_resource_group.playground](https://registry.terraform.io/providers/hashicorp/azurerm/3.67.0/docs/resources/resource_group) | resource |
| [azurerm_subnet.this](https://registry.terraform.io/providers/hashicorp/azurerm/3.67.0/docs/resources/subnet) | resource |
| [azurerm_virtual_network.this](https://registry.terraform.io/providers/hashicorp/azurerm/3.67.0/docs/resources/virtual_network) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_location"></a> [location](#input\_location) | The Azure Region where the resources should exist | `string` | n/a | yes |

## Outputs

No outputs.
<!-- END_TF_DOCS -->
