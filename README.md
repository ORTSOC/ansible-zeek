ansible-zeek
=========

Deploys Zeek to specified machine.

Requirements
------------

- Debian 10
- sudo
- ssh

Role Variables
--------------

- alert_email: email address to send alerts to.
- interface: The network interface to read to traffic over. Can be found with `ip dev`. ex. eth0, wlan0, etc. 
- networks: a list of subnets in CIDR format to listen to traffic over using the specified interface.
load_script: a list of scripts to load, using paths. See below example.

Example Playbook
----------------

```yaml
alert_email: test@ortsoc.email
interface: eth0
networks:
 - 10.0.0.0/24
 - 192.168.0.0/24
load_script:
 - policy/misc/capture-loss
```

License
-------

GPL3

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
