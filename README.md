# Linera Ansible Playbook

This repository contains an Ansible playbook for setting up and managing Linera nodes. It is designed to help you quickly deploy and configure Linera nodes across various environments.

## Features

- Automated Linera node setup
- Configuration management for nodes
- Support for multiple environments

## Prerequisites

Before you begin, ensure you have the following installed on your machine:
- Ansible 2.9 or higher
- SSH access to the target servers
- Python 3.9 or higher

## Installation

1. Clone this repository to your local machine.
2. Copy the sample inventory file:

```sh
cp inventory.yml.sample inventory.yml
```

3. Fill out the inventory information in `inventory.yml` with details of your target servers.
4. Run the Ansible playbook:

```sh
ansible-playbook main.yml -e target=canarynet
```

## Configuration

The playbook uses variables to customize the Linera node setup. These variables can be found and modified in the `vars/main.yml` file. 
Common configurations include network id, peers, and validator peers.

## Running the Playbook

To deploy Linera nodes to your specified environment, use the following command:

```sh
ansible-playbook main.yml -e target=<environment>
```

Replace `<environment>` with your target environment, such as `canarynet`, `testnet`, or `mainnet`.

## Support

For issues and questions about this playbook, please open an issue in the GitHub repository.

## Contributing

Contributions to this playbook are welcome. Please fork the repository, make your changes, and submit a pull request.

## License

This Ansible playbook is released under the MIT License. See the LICENSE file for more details.
