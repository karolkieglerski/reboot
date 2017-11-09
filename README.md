reboot 
=========

[![Build Status](https://travis-ci.org/kilerkarol/reboot.svg?branch=master)](https://travis-ci.org/kilerkarol/reboot)

Role for restart nodes and wait to nodes come back over ssh.

Role Variables
--------------

Default variables for that role
```
    reboot_delay_on: 2
    reboot_desc: "Ansible reboot"
    reboot_ignore_errors: true
    reboot_come_back: 30
    reboot_timeout: 360
```

Variable set to get default ansible variable form inventory `ansible_port` 
```
    ssh_port: "{{ ansible_port }}"
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: kilerkarol.reboot, tag: reboot }

License
-------

BSD