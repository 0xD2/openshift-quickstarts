
#### Ansible scheme of project
```
project/  
├─ hosts/
│  ├─ shared-secrets.yml  # encrypted shared vars
│  ├─ shared-vars.yml     # not encrypted shared vars
│  ├─ internal/
│  │  ├─ inventory        # inventory file with definitions of all hosts
│  │  ├─ secrets.yml      # encrypted vars for this environment
│  │  └─ groups_vars/     # same as in standard project
│  │  │  ├─ all.yml       
│  │  │  └─ group.yml
│  │  └─ host_vars/       # same as in standard project     
│  │     └─ host1.yml
│  ├─ staging/            # directory for other environment
│  │  └─ ...
│  ├─ production/
│     └─ ...
├─ roles/                 # all ansible roles used in playbooks
│  ├─ role1/
│  │  ├─ main.yml
│  │  └─ ...
│  └─ role2/
│     └─ ...
├─ tasks/
|  └─ load_vars.yml       # special task for loading vars
├─ ansible.cfg            # ansible config file
├─ playbook1.yml          # here we put our playbooks
└─ playbook2.yml
```
