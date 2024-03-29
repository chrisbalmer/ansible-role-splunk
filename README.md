Splunk
======

Installs Splunk and configures the service.

Requirements
------------

None

Role Variables
--------------

```yaml
splunk_key_general: password
```

This is the general pass4SymmKey entry in `server.conf`. Use a hashed password if you don't want Splunk overwriting it with a hashed version at startup.

```yaml
splunk_ssl_password: password
```

This is the sslPassword entry in `server.conf`. Use a hashed password if you don't want Splunk overwriting it with a hashed version at startup.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: chrisbalmer.splunk-installation }

Tasks
-----

- [ ] Move firewall settings to dedicated firewall role.
- [ ] Pull existing passwords from conf files if variable isn't defined.

License
-------

MIT

Author Information
------------------

Chris Balmer
