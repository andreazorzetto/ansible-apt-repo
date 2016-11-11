apt-repo
=================

Configure internal apt mirror for ubuntu trusty (14.04)
Install the extra repos:
- php5.6
- grafana
- influxdb
- openjdk for all java in ubuntu 14

Install extra repo keys
Update cache


Role Variables
-----------------


apt_mirror


How to RUN the role
-----------------


__for AWS servers__
```
ansible-playbook -i run/inventories/aws run/playbooks/apt-repo-aws.yml
```

__for Staging servers__
```
ansible-playbook -i run/inventories/stag run/playbooks/apt-repo-stag.yml
```

__for Pre Production servers__
```
ansible-playbook -i run/inventories/preprod run/playbooks/apt-repo-preprod.yml
```

__for Production servers__
```
ansible-playbook -i run/inventories/prod run/playbooks/apt-repo-prod.yml
```

__for Vagrant tests__ (password: vagrant)
```
vagrant up
ansible-playbook -i run/inventories/vagrant run/playbooks/apt-repo-vagrant.yml -k
```
