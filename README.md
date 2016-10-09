# ansible-role-dkhabarov-repo
Add my [personal deb repo](https://saymon21-root.pro/deb-repo/).

## Requirements

apt-transport-https

## Installation

Write to requirements.yml

        - src: https://github.com/dkhabarov/ansible-role-dkhabarov-repo.git
          name: dkhabarov.ansible-role-dkhabarov-repo

Run install command:

        ansible-galaxy install -i -f -r requirements.yml
