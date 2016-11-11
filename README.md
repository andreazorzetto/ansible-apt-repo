Ansible APT Repo role
=================

Configure an ubuntu server as a client to point to aptmirror internal repository, previously set up with [ansible aptmirror role](https://galaxy.ansible.com/andreazorzetto/Ubuntu-Aptmirror/).

Tasks:
-----------------
- Install extra repo keys
- Update cache


Role Variables
-----------------


```apt_mirror``` with the aptmirror server ip address

A list of repositories exported on the apt mirror server needs to be created like the example one available in the ```vars``` of this role.

Example of values:

```
repos:

  - title: ubuntu
    source: true
    distro:
      - trusty
      - trusty-security
      - trusty-updates
    components:
      - main
      - restricted
      - universe
      - multiverse

  - title: ondrej
    source: true
    distro:
      - trusty
    components:
      - main

  - title: grafana
    source: false
    distro:
      - wheezy
    components:
      - main
```
