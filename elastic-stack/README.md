## Ansible project for filebeat installation and setting up
### Requirements
```
ansible-galaxy collection install ansible.posix //to manage firewalld ports
```
### For Develop
```
ansible-playbook -i inventory/dev/hosts main.yaml
```

### For Hml
```
ansible-playbook -i inventory/dev/hosts main.yaml
```

### For Production
```
ansible-playbook -i inventory/prod/hosts main.yaml
```

### Project Structure based on roles
.
├── ansible.cfg
├── debug.yaml
├── inventory
│   ├── dev
│   │   ├── group_vars
│   │   │   └── all.yml
│   │   └── hosts
│   ├── hml
│   │   ├── group_vars
│   │   │   └── all.yml
│   │   └── hosts
│   └── prd
│       └── group_vars
│           └── all.yml
├── main.yaml
└── roles
    └── filebeat
        ├── config
        │   ├── README.md
        │   ├── defaults
        │   │   └── main.yml
        │   ├── files
        │   ├── handlers
        │   │   └── main.yml
        │   ├── meta
        │   │   └── main.yml
        │   ├── tasks
        │   │   └── main.yml
        │   ├── templates
        │   │   └── filebeat.yml.j2
        │   ├── tests
        │   │   ├── inventory
        │   │   └── test.yml
        │   └── vars
        │       └── main.yml
        └── install
            ├── README.md
            ├── defaults
            │   └── main.yml
            ├── files
            │   ├── GPG-KEY-elasticsearch
            │   └── filebeat-9.0.1-x86_64.rpm
            ├── handlers
            │   └── main.yml
            ├── meta
            │   └── main.yml
            ├── tasks
            │   └── main.yml
            ├── templates
            ├── tests
            │   ├── inventory
            │   └── test.yml
            └── vars
                └── main.yml
 
