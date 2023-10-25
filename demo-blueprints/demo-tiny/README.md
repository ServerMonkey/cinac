# CinaC blueprint: Demo Tiny - A single Debian VM

This is a Demo blueprint for https://github.com/ServerMonkey/cinac

The goal of this blueprint is to install and set up a single Debian VM with a
generic configuration.

To install a blueprint, copy the blueprint folder into $HOME/. cinac/ on the
CinaC host.

CinaC blueprints are made of a folder that contains some or all of the
following files:

* Inventorymaker inventory file **inventory/\<NAME\>.csv**  
  *At least one CSV file is required.*  
  This file contains the required information for the CinaC host, to establish
  an SSH connection to the guest machine. Here you set basic variables like
  hostname, superuser login or name of a Golden Image to load.

* CinaC blueprint initialzation file: **bp.ini**  
  *Required*  
  This file tells CinaC what packages are required and how to set up the
  networks and configure guest machines. This file tells CinaC how to build the
  entire environment.

* Blueprint documentation file: **README.md**  
  *Required*  
  Self-explaning.

* WildWest configuration file: **ww.cfg**  
  *Not required*  
  This file tells WildWest what playbooks and scripts are enabled and can be
  used during the configuration of a guest.

* Ansible configuration: **ansible.cfg**  
  *Not required*  
  Custom environment specific Ansible configuration.

In addition, you can include blueprint specific folders for extra configuration
files. Use this if you do not which do distribute specific playbooks or scripts
via APT or fastpkg.

* Additional VM templates:
  **vm_templates/\<NAME\>.xml**  
  *Not required*  
  These xml files will be copied into the vmh (virtualmachinehandler)
  IMMUTABLE folder.

* Additional playbooks:
  **playbooks/\<ANY_FILES\>**  
  *Not required*

* You can even add additional files and folder of your own. But avoid binary
  files. The goal of a blueprint is to be representet as code only.