# Baremetal-Install-Multiple-Servers
This Repository contains Cisco Intersight Workflows to Install ESXi, Windows Server and RHEL over multiple UCS X Series Blades at once on local disks. May also work for other UCS Standalone or IMM Servers but hasn't been tested at the moment. 

## Work in Progress...

### Prerequisites

- A known working Cisco UCS Server Template to derive Server Profiles for each blade.
- M2 RAID controllers on each blade with a minimum of

### Import

### Configuration

### Known Issues

- The workflows will NOT activate the server profiles if there are policies changes that require a second reboot. If the storage policy is creating the virtual drive for the first time, you may want to first activate a working server profile to create the virtual disks before exeecuting the workflow. Workaround: deploy derived server profiles before running the workflow the first time

- Workflows will fail if there are already server profiles with the same name or if one of the blades already have a profile attached. Workaround: Unassign profile from servers or modify the workflows to onòy perform the operating system install

- ...