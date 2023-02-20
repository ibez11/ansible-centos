# Infra
Contains the ansible scripts for all Project

# Set Up
Please install ansible server in you laptop

IMPORTANT: Profile name must be <project>-prd in hosts

On linux client config

1. Create file for access no need password
    - nano /etc/sudoers.d/<name_user>
    - <name_user> ALL=(ALL) NOPASSWD: ALL

## Test connection
```
ansible <host> -m ping
```

## Apply Changes
```
ansible-playbook 01-app.yml -e "hosts=<hosts> env=<ENVIRONMENT>"
```

## Unlock
```
git-crypt unlock <PATH_TO_KEY>
```

## Lock
```
git-crypt lock
```

## Check Status
```
git-crypt status
```
