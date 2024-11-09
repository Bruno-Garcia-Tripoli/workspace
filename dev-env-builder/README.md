# Development Environment Builder

## Getting Started

### Pre-requirements

Ensure the following packages are installed:

- git
- python
- ssh
- pipx

```
sudo apt-get install git python3 ssh pipx
pipx ensurepath
```

### Install ansible

Install ansible from the terminal. Follow
the [installing guide](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-and-upgrading-ansible-with-pipx).

```
pipx install --include-deps ansible
```

### Create or copy the `vars.yaml` file

Create the file `vars.yaml` in recipes/group_vars or copy and rename the file `recipes/group_vars/vars.yaml.dist`.
Edit the file and set up the environment variables.

Once the playbooks has been executed successfuly is recommended to save the `vars.yaml` file.

### Run the playbooks

Playbooks are recipes to get things installed. You can run them individually, or you can run all of them at once (
recommended) by running `_all,yaml`.
To run them there are a few ways:

`mkdir -p /tmp/.ansible/tmp`

- If you want it to prompt for the user password:

```
time ansible-playbook -i inventory.ini recipes/_all.yaml -K
```

