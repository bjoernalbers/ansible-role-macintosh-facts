# Ansible Role: macintosh_facts

[![Build Status](https://travis-ci.org/bjoernalbers/ansible-role-macintosh-facts.svg?branch=master)](https://travis-ci.org/bjoernalbers/ansible-role-macintosh-facts)

An Ansible Role to install custom facts on Macintosh Computers for reporting.
Here's a sample of these new facts:

    $ ansible -m setup belladona -a filter=ansible_local
    belladona | SUCCESS => {
        "ansible_facts": {
            "ansible_local": {
                "macintosh": {
                    "computer_information": {
                        "info1": "Office 42",
                        "info2": "Tim Cook",
                        "info3": null,
                        "info4": null
                    },
                    "marketing_name": "Mac mini (2018)",
                    "model_identifier": "Macmini8,1",
                    "model_name": "Mac mini",
                    "serial_number": "C03ZN6AMJYW0"
                }
            }
        },
        "changed": false
    }


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
