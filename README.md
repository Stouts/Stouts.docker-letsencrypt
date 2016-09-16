Stouts.docker-letsencrypt
=========================

Ansible role to install SSL certificates from Letsencrypt

#### Variables

```yaml
letsencrypt_enabled: yes

letsencrypt_home: /opt/letsencrypt
letsencrypt_image: quay.io/letsencrypt/letsencrypt
letsencrypt_keep: true
letsencrypt_email: "{{ansible_user_id}}@{{inventory_hostname}}"
letsencrypt_domains: ["{{inventory_hostname}}"]
letsencrypt_stop_services: [nginx, apache]

letsencrypt_renew: false
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
