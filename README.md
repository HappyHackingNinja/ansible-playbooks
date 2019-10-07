# Ansible Playbooks

## Usage

```sh
# Setup environment on MacOS
ansible-playbook -v setup-macos-environment.yml

# Setup development environment on Arch Linux
ansible-playbook -v -i inventories/playground -K --ask-vault-pass setup-arch-dev-environment.yml

# Setup Jenkins CI
ansible-playbook -v -i inventories/playground --ask-vault-pass setup-jenkins-ci.yml
```
