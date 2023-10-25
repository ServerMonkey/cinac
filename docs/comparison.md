## COMPARISON

How does CinaC compare to other solutions?

**vs. KVM/QEMU, VirtualBox, ...**

CinaC heavily uses KVM/QEMU through libvirt, but it's more than just a
virtualization platform (hypervisor). It uses 'vmh' to make libvirt easier to
use and more automated for larger environments and mass deployments. Unlike
most virtualization platforms, that only manage virtual machines, CinaC has
integrated asset inventory management, deployment, provisioning, configuration,
and package management build into.

**vs. Proxmox**

* CinaC is much more minimalistic and has a narrow focus on how to facilitate
  VM deployment. Where Proxmox comes with lots of possibilities.
* CinaC can also manage physical devices.
* CinaC has file and software sourcing/installation where Proxmox does not.
* CinaC is a Debian package, where Proxmox is a Linux distribution. Usually you
  don't install Proxmox directly on a workstation, where CinaC encourages to be
  installed and used on desktop workstations as well as on servers.
* CinaC tries to complement Debian Stable, where Proxmox comes with its own
  kernel and QEMU/LXC package.
* CinaC tries to give the user maximum flexibility on how to set up their
  system, where Proxmox is a pure virtualization platform.

**vs. OpenStack**

* CinaC is much more minimalistic and has a narrow focus on how to facilitate
  VM deployment. Where OpenStack comes with lots of possibilities.
* The initial setup of CinaC is easier than OpenStack.
* CinaC can run on a single host where OpenStack is usually intended for at
  least two or more servers.
* OpenStack uses their own platform called: 'projects' to facilitate
  networking, storage and so on. In CinaC Everything is broken down into
  smaller Debian packages that operate independently of each other and only
  communicate via CLI and text based configuration file.
* OpenStack tries to abstract away the underlying systems from the end-user and
  presents a web application as front-end. CinaC sticks to the Linux/*NIX
  philosophy.
* The intended use of OpenStack is to be the base of a cloud provider. CinaC
  only tries to be a generic infrastructure management system that complements
  the existing Debian framework, instead of being a cloud-only product.

**vs. Vagrant**

* Vagrant simplifies VM deployment, just like CinaC.
* CinaC can manage other devices than just VMs. Vagrant is only for VMs.
* CinaC has file and software sourcing/installation where Vagrant does not,
  except for Golden Images.
* Vagrant inventory and VM management is based on creating VMs inside folders.
  CinaC manages hosts via CSV inventory files and libvirt.
* CinaC uses CSV and INI style configuration files and YAML for VM
  provisioning. Vagrant uses Ruby style and YAML.
* CinaC provisions VMs strictly via SSH. Vagrant usually uses cloud-init or
  other.
* CinaC is stricter on how to do things. Vagrant has lots of different
  possibilities.

**vs. Ansible AWX / Ansible Tower**

* CinaC is much more minimalistic and has a narrow focus on how to do things.
  AWX and Ansible Tower have different 'Platform components'.
* CinaC has integrated VM deployment, AWX focus is provisioning and
  configuration.
* Ansible Tower is a web application, where CinaC is a CLI application, but it
  comes with a CLI based GUI, 'tgui'.
* CinaC uses the CLI tool 'wildwest' to facilitate what Ansible Tower does via
  a web front-end. But they are very different in how they do things. But the
  underlying technology is the same: Ansible.
* AWX comes with a REST API. CinaCs intended use is via CLI and blueprints.
* Ansible Tower comes with 'Ansible Content Collections', CinaC comes with some
  ready to use Ansible collections and roles, made to work with CinaC.

**vs. ESXi**

* ESXi is a proprietary virtualisation stack with tons of different solutions.
* ESXI is meant for very large corporate environments. CinaC is ment to be used
  for smaller environments.

**vs. DebianLAN**

* CinaC and DebianLAN have several similarities
* They both use ansible and Debian as management systems.
* They are both very minimalistic compared to other solutions like OpenStack or
  ESXi.
* DebianLAN is more a tutorial on how to create automated networks with Debian
  than a fully automated solution.