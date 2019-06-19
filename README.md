gabops.repo-percona
=========

Installs Percona (https://www.percona.com) repository.

Requirements
------------

None.

Role Variables
--------------
This role uses the variables with the next default values:

  RedHat os family:
  - `percona_repo_url`: https://repo.percona.com/yum/percona-release-latest.noarch.rpm
  
  - `percona_repo_gpg_key_url`: https://www.percona.com/downloads/RPM-GPG-KEY-percona

  Debian os family:
  - `percona_repo_url`: "https://repo.percona.com/apt/percona-release_latest.{{ ansible_distribution_release }}_all.deb"

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
2 - Overwritting the a value for using for example another url repo
```yaml
    - hosts: servers
      vars:
        percona_repo_url: http://another_url/foo/bar.deb
      roles:
         - { role: gabops.repo-percona }
```

License
-------

MIT

Author Information
------------------

Gabriel Suarez (gabops)
