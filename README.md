[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-pyguy.prometheus__ipmi__exporter-blue.svg)](https://galaxy.ansible.com/pyguy/prometheus_ipmi_exporter)

Prometheus IPMI exporter
========================

This role installs ipmi exporter for Prometheus using [this repo](https://github.com/soundcloud/ipmi_exporter).

Requirements
------------

This role installs the following package dependencies:
  * `git`
  * `golang`
  * `freeipmi-tools`

you also need to have a running golang environment.

Tested platforms are:

  * Ubuntu
    * bionic
    * xenial
    * trusty
    * precise


  * Debian
    * stretch
    * jessie
    * squeeze
    * wheezy


  * CentOS 7

Role Variables
--------------

* `GO_PATH` var is for the golang environment to work which default is `/opt/go`

* `GO_BIN` is go command binary file which default is `go`, in some distributions
  it sould be the command absolute path.

* `ipmi_config_path` is the IPMI config dir which default is `/opt/go/bin`

* `ipmi_listen_address`  is the address/port to listen on which default is `:9290`

*  `exclude_sensor_ids` option can be used in `ipmi.yml` file, you can find them [here in Wiki](https://github.com/pyguy/ansible-prom-ipmi-exporter/wiki/IPMI-Sensors)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: localhost
      roles:
         - { role: prometheus-ipmi-exporter }
```

Sample grafana graph
--------------------
![ipmi-general-status-grafana](/imgs/ipmi-general-status-grafana.png)
![ipmi-graphs-grafana](/imgs/ipmi-graphs-grafana.png)

License
-------

GPLv2
