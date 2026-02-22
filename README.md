# Ansible_Training
This repo is made to track some ansible playbook, adhoc commands and notes

# Notes for later:
## General notes -> Ansible is AUTOMATION TOOL
* Ansible was required as the other competitors (salt, etc) were not agentless. i.e They required agents to be setup on the target VM's
* Ansible is completely agentless and uses simple yaml which further reduces and learning curve which you had with other technologies
* You need only to install ansible on the CONTROL NODE and you can manager all the VM"S (MANAGER NODES) from the control node
* Need to have python installed in both the CONTROL AND MANAGE nodes

## Use cases of Ansible:
* Provising of resources -> s3 bucket, ec2 instance etc
* VM config management 
* Deploy -> use ansible to deploy resources to multiple VM's
* Network Automation
