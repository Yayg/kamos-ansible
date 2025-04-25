# Ansible Repository

This repository is designed to configure servers using Ansible with the `ansible-pull` command. It includes roles for installing unattended upgrades and setting up Kind.

## Directory Structure

```
ansible-repo
├── roles
│   ├── base
│   │   ├── tasks
│   │   │   └── main.yml
│   │   └── defaults
│   │       └── main.yml
│   ├── kind
│   │   ├── tasks
│   │   │   └── main.yml
│   │   └── defaults
│   │       └── main.yml
├── inventory
│   └── hosts
├── ansible.cfg
├── pull.yml
└── README.md
```

## Roles

### Base Role

The **base** role is responsible for installing and configuring unattended upgrades on the server. It ensures that the necessary packages are installed and configured properly.

### Kind Role

The **kind** role installs the dependencies required for Kind and sets up Kind itself. This role automates the installation process to ensure a smooth setup.

## Usage

To use this repository, you can run the following command on your server:

```bash
ansible-pull -U <repository-url> -i inventory/hosts pull.yml
```

Replace `<repository-url>` with the URL of this repository.

## Requirements

- Ansible must be installed on the server.
- Ensure that the inventory file is correctly configured with the target hosts.

## Contributing

Feel free to submit issues or pull requests to improve this repository.