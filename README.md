# Packer templates for Windows Server using vSphere-ISO provider

## Note: this code is compatible with Packer v1.5.x or previous versions. For Packer v1.6.x or later use this [link](https://github.com/guillermo-musumeci/packer-vsphere-iso-windows-v2) 

This repository contains **HashiCorp Packer** templates to deploy **Windows Server** distros in **VMware vSphere (with vCenter)**, using the **vsphere-iso** builder.

These templates creates the Template (or VM) directly on the vSphere server and install the latest VMware Tools.

# Content: #

Windows Server 2016:
* [win2016.base/win2016.base.json](./win2016.base/win2016.base.json) --> Windows Server 2016 Packer JSON file Base
* [win2016.base/autounattend.xml](./win2016.base/autounattend.xml) --> Answer file for unattended Windows setup

Windows Server 2019:
* [win2019.base/win2019.base.json](./win2019.base/win2019.base.json) --> Windows Server 2019 Packer JSON file Base
* [win2019.base/autounattend.xml](./win2019.base/autounattend.xml) --> Answer file for unattended Windows setup

Scripts:
* [scripts/disable-network-discovery.cmd](./scripts/disable-network-discovery.cmd) --> Script to Disable network discovery
* [scripts/disable-winrm.ps1](./scripts/disable-winrm.ps1) --> Script to Disable WinRM
* [scripts/enable-rdp.cmd](./scripts/enable-rdp.cmd) --> Script to Enable Remote Desktop
* [scripts/enable-winrm.ps1](./scripts/enable-winrm.ps1) --> Script to Enable WinRM
* [scripts/install-vm-tools.cmd](./scripts/install-vm-tools.cmd) --> Script to Install VMware Tools
* [scripts/set-temp.ps1](./scripts/set-temp.ps1) --> Script to Set Temp Folders

Tested with **VMware ESX 6.7** | User: Administrator | Password: S3cr3t0!

# Requirements: #

* Packer --> https://www.packer.io

# How to use: #

execute **packer build win2016.base.json**

# Credits: #

Inspired by [Stefan Scherer](https://github.com/StefanScherer/packer-windows), [Mischa Taylor](https://sheska.com/automating-windows-server-2016-installs) and [Dmitry Teslya](https://dteslya.engineer/automation/2018-12-20-creating_vm_templates_with_packer) works.
