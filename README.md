# Ansible Server Roles
Configure servers for provisioing using Ansible and deployed via AWX. I targeted Debian/Ubuntu with this repository, but other distros may work as well. 

## Prerequisites

- Ansible
- AWX

## Installation

### In AWX
1. Create source control, make sure to use their respective credential types too
2. Create a project and point to your fork and branch in Github, GitLab, etc. Make sure to check the box to update on launch. This is pull the latest commit into AWX
3. Create an inventory with the servers you would like to target
4. Create a Template and choose **Job Type** of `run` then select for inventory and project from the dropdowns. Set your playbook as well. You can set your execution environment if you want, but it shouldn't be required. 
5. In the template, set your credentials to log on to the servers (SSH keys recommended).
6. Save the template and **Launch** the job

## Usage

- To configure the servers, run `ansible-playbook -i inventory/hosts playbook.yml`.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Test your changes.
5. Submit a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
