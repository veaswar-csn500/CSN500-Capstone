# Summary of Checkpoint3


## Table of Contents

1 - [Project Summary](#project-summary)

2 - [Initial Configuration](#initial-configuration)

3 - [Template .json files](#template-json-files)

4 - [Bash script to deploy VM](#bash-script-to-deploy-the-vms)

5 - [CLI commands to set static IP](#cli-command-to-set-static-ip) 

6 - [Table](#sample-table)

7 - [IIS Installation](#iis-installation)

8 - [Diagram](#mydiagram)


## Project Summary

- Configure a DNS server in WS-XX

- Configure DNS server and name on LS-XX, WC-XX and LR-XX

- Install, configure and SSh, FTP, MariaDB,Apache services and test them on the Windows and Linux Servers

- Configure the iptables and firewall on the Jump Server to allow traffic from your networks to access services on standard ports

- XX - Unique student id number

- XXXXXX - Student-RG number in Azure portal

## Initial Configuration

- Make sure to deploy all VMs and to enable iptables on LR-XX and LS-XX

- Make sure the VMs get the respective static IPs. (LS-XX : 172.17.XX.36, WS-XX : 172.17.XX.37, LR-XX : 192.168.XX.36)

- DNS to be configured in WS-XX and make sure the LS-XX,LR-XX and WC-XX gets the DNS name.


## Template .JSON Files

- [WC-48](WC-48.json)

- [WS-48](WS-48.json)

- [LR-48](LR-48.json)

- [LS-48](LS-48.json)

## Bash Script to Deploy the VMs

- [Deploy VMs](VMDeploy.bash)

## CLI command to set static IP
```bash
- az network nic ip-config update --name LR-XX --resource-group Student-RG-XXXXXX --nic-name LR-XX --private-ip-address 192.168.XX.37

- az network nic ip-config update --name LR-XX --resource-group Student-RG-XXXXXX --nic-name LR-XX --private-ip-address 192.168.XX.36

- az network nic ip-config update --name WS-XX --resource-group Student-RG-XXXXXX --nic-name WS-XX --private-ip-address 172.17.XX.50

- az network nic ip-config update --name WS-XX --resource-group Student-RG-XXXXXX --nic-name WS-XX --private-ip-address 172.17.XX.37

- az network nic ip-config update --name LS-XX --resource-group Student-RG-XXXXXX --nic-name LS-XX --private-ip-address 172.17.XX.51

- az network nic ip-config update --name LS-XX --resource-group Student-RG-XXXXXX --nic-name LS-XX --private-ip-address 172.17.XX.36

- az network nic update --name LR-XX --resource-group Student-RG-XXXXXX --ip-forwarding true
```

## Sample Table

| Student Details | - |
| - | - |
| Name | Vishal Easwar |
| ID | 126507201 |
| Section | CSN 500 NBB | 


## IIS Installation

- In WS-XX, after deploying VM, open **Server Manager**.
- Click on **Add Roles and Features**.
- Click next till we get a window to select the roles to install.
- Select **IIS** from that and click next.
- A windows will pop up asking for features to be installed. Click **Add features**.
- And continue to click on Next till the installation starts
- Wait for the installation to be over and IIS role should be installed in the WS-XX. 

## My_Diagram

<img src="./IND6image.png"
     alt="ind6image"
     style="float: center; margin-right: 10px;" />