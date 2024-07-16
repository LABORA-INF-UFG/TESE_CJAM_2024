# Deployment Environment and Component Configuration
In this experiment, we will address the deployment process of the UE-non-3GPP, N3IWF, and Free5GC components in a cloud environment, utilizing three virtual machines provisioned in a cloud environment. Figure below illustrates the topology used in this experiment. In the figure, we can see that three VMs are depicted: the first for the provisioning of the UE-non-3GPP, the second for the provisioning of the N3IWF, and the third dedicated to running the remaining network functions that comprise the 5G core.

<p align="center">
    <img src="../images/topology_install.png"/> 
</p>

## Steps for installing and configuring the Prototype

The content described in this repository was tested in [Digital Occean](https://www.digitalocean.com/) cloud environment. 1º VM where free5GC will run (except N3IWF) and 2º VM where the N3IWF, each of them with the following configurations:
* SO: Ubuntu 20.04 (LTS) x64
* Uname -r: 5.4.0-122-generic
* Memory: 4 GB
* Disk: 80 GB

#### Before starting
The development environment setup is exec by Ansible. Before starting it is necessary to access via SSH each one of the VM's and execute the following command to install some basic dependencies.
```
sudo apt update && apt -y install python && sudo apt -y install git && sudo apt -y install ansible && sudo apt -y install net-tools && sudo apt -y install traceroute
```

Clone the project with the following command:
```
apt update && git clone https://github.com/LABORA-INF-UFG/TESE_CJAM_2024.git 
```


