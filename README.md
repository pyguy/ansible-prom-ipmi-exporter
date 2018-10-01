[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-pyguy.prometheus__ipmi__exporter-blue.svg)](https://galaxy.ansible.com/pyguy/prometheus_ipmi_exporter)

Prometheus IPMI exporter
========================

This role installs ipmi exporter for Prometheus

Requirements
------------

This role installs the following package dependencies:
  * `git`
  * `golang`
  * `freeipmi-tools`

you also need to have a running golang environment.

Role Variables
--------------

`GO_PATH` var is for the golang environment to work which default is `/opt/go`

`ipmi_config_path` is the IPMI config dir which default is `/opt/go/bin`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
         - { role: prometheus-ipmi-exporter }

License
-------

BSD
