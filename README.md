## phpmemcachedadmin

[![CI](https://github.com/Oefenweb/ansible-phpmemcachedadmin/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-phpmemcachedadmin/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-phpmemcachedadmin-blue.svg)](https://galaxy.ansible.com/Oefenweb/phpmemcachedadmin)

Set up [phpMemcachedAdmin](https://code.google.com/p/phpmemcacheadmin/) (Memcached server admin in php for monitoring and debugging).

#### Requirements

None

#### Variables

* `phpmemcachedadmin_version`: [default: `1.2.2-r262`]: Version to install

* `phpmemcachedadmin_install_dirs`: [default: `[]`]: Install directory declarations
* `phpmemcachedadmin_install_dirs.{n}.dest`: [required]: The remote path of the installation (e.g. `/var/www`)
* `phpmemcachedadmin_install_dirs.{n}.owner`: [required]: The name of the user that should own the directories and file(s) that need to be writable
* `phpmemcachedadmin_install_dirs.{n}.group`: [optional, default `owner`]: The name of the group that should own the directories and file(s) that need to be writable
* `phpmemcachedadmin_install_dirs.{n}.state`: [optional, default: `present`]: State

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - oefenweb.phpmemcachedadmin
  vars:
    phpmemcachedadmin_install_dirs:
      - dest: /var/www
        owner: www-data
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-phpmemcachedadmin/issues)!
