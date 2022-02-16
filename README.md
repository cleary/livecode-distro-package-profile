# Description

# TO UPDATE: ansible package profiles to help build a livecoding focussed livecd

# Usage

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
