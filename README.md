# Overview
This role installs and configures cloud-init and it's customization for your platform.
This role requires root permissions. It must be called as root. This needs to be managed at the ansible or playbook level.

Some applications require a valid entry in /etc/hosts for the local ip. This role customizes the installation for setting a correct /etc/hosts.

Minimal facts need to be gatherd.

# Variables

| Name  | Type | Required | Default Value | Description |
| ----- | ---- | -------- | ------------- | ----------- |
| cloud-init-platform | string | no | `nil` | Label of the virtualization platform |
| cloud_init_interface_name | string | no | `eth0` | Name of thr primary network interface |
| cloud_init_enable_updates | boolean | no | `false` | Perform a system upgrade on first boot |

# Supported virtualization platform

This role supports the following platforms:
- pve: Proxmox VE

Platforms supported in the future:
- esx: VmWare ESX virtualization platform
- vcd: VmWare vCloud Director
- gcp: Google Cloud Provider
- aws: Amazon Web Services
- azure: Microsoft Azure Cloud

# Automatique Testing

This role is tested using Molecule against:
- Python 3.7, 3.8 and 3.9
- CentOS 7/8/9
- Debian 9/10/11/12

# Help

I can't test on every virtualization platform.
Please help out by trying out on different platforms and reporting status, successes or failures.