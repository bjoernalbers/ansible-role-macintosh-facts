# Ansible Role: macintosh_facts

An Ansible Role to install custom facts on Macintosh Computers for reporting.
Currently the serial number is returned.


## Requirements

The target host must be a Mac.
You also have to become root on this host for fact installation.


## Role Variables

None.


## Dependencies

None.


## Example Playbook

```yml
---
- name: Install custom facts for Macintosh
  hosts: macs
  # You have to become root to install the facts.
  become: yes
  roles:
     - role: bjoernalbers.macintosh_facts
```


## License

This Ansible role is released under the [MIT License](LICENSE.txt).
