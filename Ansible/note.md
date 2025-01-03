# Ansible

## Principles

* Ansible was created to provide an simple and securized automation tool.
* Ansible is now owned by Red Hat and easily integrable with other Red Hat' solutions.
* In general, Ansible can manage complex workflows but it can also automate deployments, manage configurations, orchestrate tasks and manage events.
* The advantage of Ansible is its agent-less functionning. Indeed, it only requires to have an SSH connection and a minimal installation of Python.
* Ansible can execute tasks in parallel on different machines but it need to wait thet completion of each tasks for all the machines.
* In theory, Ansible can only be installed on Linux and MacOs operation systems.
* Ansible uses Yaml to write its playbooks.
* Ansible works by executing tasks on distant hosts. These hosts are defined in an inventory that can be static or dynamic. Static inventory are files listing target servers.
* A playbooks is divided into tasks and hosts components.

## Main commands

* `ansible-playbook -i inventory playbook.yaml --check` : This command check if the code works correctly before running it.

## Good practices and tips

### Installation

The cleanest way to install Ansible is to use a pyenv or user space. This way to proceed allows to choose precisely the Ansible's version to install. This is an installation script to install Ansible in an user's python space.

```sudo apt update
sudo apt -y upgrade
sudo apt install -y build-essential libssl-dev libffi-dev python3-dev python3-pip
pip3 install ansible --user
```

To choose a specific version of ansible to install:

```pip3 install --user ansible==4.1.0
```

### Playbook's example

```- name: Installation de Nginx sur un serveur
  hosts: webservers
  tasks:
    - name: Installer Nginx
      ansible.builtin.apt:
        name: nginx
        state: present
```
