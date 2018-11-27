# Ansible configuration and files

My personal setup for Ansible. This is a WIP.

## Encrypted files

### Password prompt
Some files are encrypted using `ansible-vault`. You can either type the password 
every time you are prompted for it, or you can create a file called `.vault_password` 
in the repository root which contains the password. Make sure to set the file
permissions to something like `600`.

### File structure of `hosts`

```yml
all:
  hosts:
    12.34.56.78:
      hostname: some-hostname-1
      ipv6: 2606:2800:220::1337
      private_ip: 10.1.0.1
    12.34.56.89:
      hostname: some-hostname-2
      ipv6: 2606:2800:220:::2018
      private_ip: 10.2.0.2
```

### File structure of `vars/users.yml`

```yml
administrators:
- {
    name: user1,
    shell: /bin/bash
  }
- {
    name: user2,
    shell: /bin/bash
  }
```
