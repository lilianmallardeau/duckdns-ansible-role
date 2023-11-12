Duck DNS Ansible Role
=====================

An Ansible role to add a cron job to update a Duck DNS record. Works on Debian-based distributions.

Requirements
------------

None

Role Variables
--------------

- `duckdns_domain`: mandatory  
Duck DNS subdomain to update. Can be a comma separated (no spaces) list of domains.

- `duckdns_token`: mandatory  
Duck DNS token

- `duckdns_log_file`: default `/var/log/duckdns.log`  
Log file to write curl request output to

- `duckdns_cron_user`: default `root`  
User to add cron job to

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: duckdns
      vars:
        duckdns_domain: "example1,example2"
        duckdns_token: "923e22d3-67cf-4243-ae34-026f159b3828"
```

License
-------

MIT
