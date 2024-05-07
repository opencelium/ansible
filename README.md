# Ansible

> [!NOTE] 
> Only available for Ubuntu systems (tested on 22.04 LTS)!

## Prepare environment

1. Install Ansible:

> [!NOTE] 
> Use default Ansible installation guide. You can find documentation here -> https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

## Install and run from playbook

2. Get oc playbook:

```
cd /etc/ansible
git clone https://bitbucket.org/becon_gmbh/opencelium.setup.ansible.git .
```

3. Add localhost in ansible

```
printf "[local]\nlocalhost ansible_connection=local" >> hosts
```

4. Run playbook

```
ansible-playbook --connection=local -e 'host_key_checking=False' playbooks/install_oc.yml
```
