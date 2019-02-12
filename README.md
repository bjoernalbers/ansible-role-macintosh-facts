# Ansible Role: macintosh_facts

An Ansible Role to install custom facts on Macintosh Computers for reporting.


## Requirements

The target host must be a Mac.


## Role Variables

None.


## Dependencies

None.


## Example Playbook

```yml
---
- name: Install custom facts for Macintosh
  hosts: macs
  roles:
     - role: bjoernalbers.macintosh_facts
```


## License

This Ansible role is released under the [MIT License](LICENSE.txt).
