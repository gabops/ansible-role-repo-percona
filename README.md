gabops.repo_percona
===================

[![Build Status](https://travis-ci.org/gabops/ansible-role-repo-percona.svg?branch=master)](https://travis-ci.org/gabops/ansible-role-repo-percona)

Installs Percona (https://www.percona.com) repository.

Requirements
------------

None.

Role Variables
--------------

| Variable | Default value | Description |
| --- | --- | --- |
| percona_repository_version | latest | The version of the package for installing the repo. |

> This role also provides the possibility of overwriting any variable in the **vars/** directory. You **never should do it**. This feature only exists for covering any unexpected scenario you might find. For doing it, just declare the variable/variables without the double underscore on your group_vars, host_vars, command line etc as you usually would do for a variable in defaults/.

Dependencies
------------

None.

Example Playbook
----------------

1 - Using the default values this roles uses:
```yaml
    - hosts: servers
      roles:
         - role: gabops.repo-percona
```
2 - Setting a custom version of the repo package
```yaml
    - hosts: servers
      vars:
        percona_repository_version: 0.1-9
      roles:
         - role: gabops.repo-percona
```

License
-------

MIT

Author Information
------------------

Gabriel Suarez (gabops)
