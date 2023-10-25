# CinaC blueprint: Demo Company - Small organization with 10 hosts

This Demo contains 10 VMs that will be installed with a more complicated setup and lots of software. The result will be a generic office network.

To start a ransomware attack run:

	$ ww -t all demo-company.playbooks ransom

## Requirements

A CinaC host with 32 GB of RAM.

You need to add a specific Windows XP image, with the name 'libvirt-img-windows-xp-pro', to your fastpkg repo. You need to download that image before you can run this blueprint.  
Alternatively add the URI of a fastpkg-repo, that contains this image, to bp.ini file under the section 'repos-fastpkg'

You can build this Windows XP image with [github.com/ServerMonkey/isoremixer](https://github.com/ServerMonkey/isoremixer) or download one from here: and add it to your internal fastpkg-repo.
