## Baisc info on PLAYBOOKS
* These are yaml files.
* A playbook is esentially a collection of **PLAYS** and each play has multiple **TASKS** in it
```
---
- name: PLAY1
  hosts: WebServer
  become: true

  tasks:
    - name: install service
      yum:
        name: httpd
        state: present
```

* To execute playbooks, you can write: 

    `ansible-playbook [-i <inventory file path>] <playbook path>`