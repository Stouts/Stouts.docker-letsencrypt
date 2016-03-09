Stouts.docker-letsencrypt
=========================

Ansible role to install SSL certificates from Letsencrypt

#### Variables

```yaml
letsencrypt_enabled: yes

letsencrypt_home: /opt/letsencrypt
letsencrypt_image: blacklabelops/letsencrypt
letsencrypt_command: install
letsencrypt_email: "{{ansible_user|default(ansible_ssh_user)}}@{{inventory_hostname}}"
letsencrypt_domain: "{{inventory_hostname}}"
```

#### Usage

Add `Stouts.docker-letsencrypt` to your roles and set vars in your playbook file.

Example:

```yaml

- hosts: all

  roles:
    - Stouts.docker
    - Stouts.docker-letsencrypt

  vars:
    letsencrypt_email: myemail@gmail.com
```

#### License

Licensed under the MIT License. See the LICENSE file for details.

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Stouts/Stouts.docker-letsencrypt/issues)!
