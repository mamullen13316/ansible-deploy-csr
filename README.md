# Deploy Cisco CSR1000V with Ansible
This Ansible playbook will deploy a Cisco CSR1000V .ova into VMware vCenter and provision using a deployment specification to pre-configure hostname, credentials, ip addressing, etc.  Additional options can be configured, to see the full list of available properties deploy a CSR1000V into vCenter manually and then on the deployed VM go to Configure and vApp Options.  Then scroll down to the `Properties` section.

## Requirements
- Ansible (verified on Ansible 2.11.2)
- pyvmomi (pip install pyvmomi)

## Usage
- Modify creds.yml.example with your vCenter credentials and save as creds.yml
- Update the variables to match your vCenter environment and desired CSR1000V settings in 'group_vars/all/vars.yml'

## Caveats
- Failed with a `KeyError` on Ansible 2.10.2
