# Day 01 — Azure VM and Apache Web Server

## Overview
As part of my 90-day Azure learning challenge, I practiced using an Ubuntu virtual machine on Microsoft Azure and accessed a basic Apache-hosted web page through the VM's public IP address.

**Status:** Exercise completed. I stopped the VM and deleted the resource groups afterward; the deployment is no longer live.

## Services and tools
- Azure Virtual Machines (Ubuntu 24.04 LTS)
- Azure Resource Groups, Virtual Network, Network Security Group (NSG)
- Azure Cloud Shell and SSH through Azure CLI
- MobaXterm for remote SSH access
- Apache HTTP Server
- Azure Monitor and Cost Management

## Procedure
1. **VM overview:** Explored an Ubuntu VM named `first-vm`, its resource group, networking, and running state.
2. **Networking:** Reviewed NSG inbound rules allowing TCP port 22 (SSH) and 80 (HTTP).
3. **Azure Cloud Shell:** Used the Azure SSH connection flow and practiced Linux terminal commands.
4. **MobaXterm:** Accessed the Ubuntu VM in a remote SSH session.
5. **Apache:** Checked Apache service activity and confirmed that `curl http://localhost:80` returned the HTML welcome page.
6. **Browser verification:** Opened the VM's public IP and saw **Welcome to Azure VM Web Server !!**.
7. **Monitoring:** Explored Azure Monitor availability and CPU metrics.
8. **Costs and cleanup:** Viewed Azure billing, stopped the VM and deleted the resource groups used in this exercise.

## Linux commands practiced
```bash
ls
cd ~
cat /etc/os-release
df -h
less /var/www/html/index.html
curl http://localhost:80
```

## Demo webpage
[`index.html`](./index.html) recreates the simple page visible in the browser screenshot. It is **not the original file** from the deleted VM.

## Key learnings
- Basics of Azure compute and networking
- SSH access via Cloud Shell and MobaXterm
- Verifying web-server responses locally and publicly
- Monitoring resources and cleaning up to limit cloud costs

## Security and screenshots
The practice NSG allowed SSH from any source. In real deployments, restrict SSH to trusted IP addresses or use Azure Bastion. **Screenshots are not included yet** because the originals display account and subscription details. Redact these before publishing.

Suggested screenshot order once redacted: VM overview → NSG rules → Cloud Shell → MobaXterm → Linux/Apache checks → Azure Monitor → Browser output.

## Next steps
Continue the 90-day Azure challenge with networking, storage, identity, and automation.

