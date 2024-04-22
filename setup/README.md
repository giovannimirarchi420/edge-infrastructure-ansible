# Installation script for the edge computer

This folder contains a script that installs all the commands and software required for a local computer to join the edge infrastructure defined by the FLUIDOS and LEGGERO projects.
This script must be executed when the computer running at the edge is started from the first time. Additional customization tasks can be carried out later, from a remote administrator, thanks to the management user created in this step.
In the end, this PC will become a mini-K3s cluster, with the possibility to offload jobs in the cloud thanks to Liqo.

The script will perform the following tasks:
1. Create a management user (mgmt)
2. Install Ansible
   1. Check if the Ansible is 2.10, if so, install the latest version
3. Clone Ansible GIT repository
4. Start Ansible script

## How to run

This script need sudo privileges to be run.

Add execution permission:
``` chmod +x edge-pc-local-setup.sh ```

Run:
``` sudo ./edge-pc-local-setup.sh ```

Or with one-command run:
``` wget -O - https://raw.githubusercontent.com/netgroup-polito/edge-infrastructure-ansible/main/setup/edge-pc-local-setup.sh | sudo bash ```