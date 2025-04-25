# kamos-ansible
Ansible repo for Kamos configuration

## Pre-requisistes

```sh
sudo apt install ansible 

echo "localhost ansible_connection=local" > /etc/ansible/hosts
```

## Installation

1. Inventory
```sh
echo "localhost ansible_connection=local" > /etc/ansible/hosts
```

2. Put the following content with the according values in a file /usr/sbin/kamos-ansible-pull
```bash
#!/bin/bash

# Run ansible-pull with authentication for a private GitHub repository
/usr/bin/ansible-pull -U https://<username>:<personal_access_token>@github.com/<username>/<repository>.git ansible-repo/pull.yml
```

3. Put the ansible.cron file in /etc/cron.d