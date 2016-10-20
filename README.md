# ansible-role-dkhabarov-repo
Add my [personal deb repo](https://saymon21-root.pro/deb-repo/).

## Requirements

apt-transport-https

## Installation

Write to requirements.yml
```yaml
        - src: https://github.com/dkhabarov/ansible-role-dkhabarov-repo.git
          name: dkhabarov.ansible-role-dkhabarov-repo
```

Run install command:

        ansible-galaxy install -i -f -r requirements.yml


Write playbook.yml 

```yaml
---
- name: apply common configuration to all nodes
  hosts: all
  user: root
  roles:
    - {role: dkhabarov.ansible-role-dkhabarov-repo, tags: install_dkhabarov_apt_repo }
```
Or in $rolename/meta/main.yml

```yaml
---
dependencies:
  - { role: dkhabarov.ansible-role-dkhabarov-repo, tags: install_dkhabarov_apt_repo }

```
Provison!
