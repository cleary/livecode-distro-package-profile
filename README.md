# Description

# TO UPDATE: ansible package profiles to help build a livecoding focussed livecd

# Usage

## For Running Machines
There is a standard workflow for incrementally pushing changes out to the GTs. This is defined by the two inventory files.  
The `host_early-adopter` file is for the first tests of changes to any role. This is run with:
```
$ ansible-playbook -i hosts_early-adopter playbooks/2204-livecode-distro.yml
```
## For Building With pyfll
```
<todo>
```

# Directory Structure
1. Playbooks define one or more Roles that you wish to be included in the build
2. Roles manage installation and configuration of a group of packages
3. Common tasks in a Role include:
    * install-packages.yml (the list of packages associated with the role)
    * preseed-debconf.yml (any package pre-configuration via debconf tool)
    * postinst.yml (any configuration required after package installation)
    * main.yml controls the calling of all tasks, and their order
