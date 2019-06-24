gabops.repo_percona
===================

[![Build Status](https://travis-ci.org/gabops/ansible-role-repo-percona.svg?branch=master)](https://travis-ci.org/gabops/ansible-role-repo-percona)

Installs Percona (https://www.percona.com) repository.

Requirements
------------

None.

Role Variables
--------------
  - `percona_repository_version`: latest

The version of the package for installing the repo.


Also this role uses internally the next variables with the next default values:

  RedHat os family:
  - `percona_repo_url`: https://repo.percona.com/yum/percona-release- {{ percona_repository_version }}.noarch.rpm

  - `percona_repo_gpg_key_url`: https://www.percona.com/downloads/RPM-GPG-KEY-percona

  Debian os family:
  - `percona_repo_url`: "https://repo.percona.com/apt/percona-release_{{ percona_repository_version }}.{{ ansible_distribution_release }}_all.deb"

The values can be overwritten as usual when calling the role. (see examples)

Dependencies
------------

None

Example Playbook
----------------

1 - Using the default values this roles uses:
```yaml
    - hosts: servers
      roles:
         - { role: gabops.repo-percona }
```
2 - Setting a custom version of the repo package
```yaml
    - hosts: servers
      vars:
        percona_repository_version: 0.1-9
      roles:
         - { role: gabops.repo-percona }
```

License
-------

MIT

Author Information
------------------

Gabriel Suarez (gabops)
