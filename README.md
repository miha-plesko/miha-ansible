# Ansible Sandbox

## Install pip requirements
Nuage vspk module requires some python libraries being installed and we have
a playbook for it:

```bash
$ ansible-playbook nuage-install.yaml
``` 

## Use vspk module via playbook
To use Nuage vspk module, you can use following playbook:

```bash
ansible-playbook nuage-generic.yaml -e @credentials.yaml -e @extra.yaml
```

Command above requires following two files:

```yaml
# extra.yaml

entity_type: Enterprise
state: present
properties:
  name: DEMO
```

```yaml
# credentials.yaml

nuage_username:   myusername
nuage_password:   mypassword
nuage_enterprise: myenterprise
nuage_url:        https://myurl:8443
nuage_version:    v5_0
```
