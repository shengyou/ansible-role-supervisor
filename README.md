# ansible-role-supervisor [![Build Status](https://travis-ci.org/shengyou/ansible-role-supervisor.svg?branch=master)](https://travis-ci.org/shengyou/ansible-role-supervisor)

* Ubuntu 14.04, 16.04
* CentOS 6, 7

Requirements
------------

* python  >= 2.6
* ansible >= 2.3


Role Variables
--------------

以下 Variables 非必填項目，想要設定自訂的 supervisor config 才需要設置。

使用方式請參考範例。

* custom_supervisor_config
* custom_process_config


Dependencies
------------

none.

Example Playbook
----------------

```
- hosts: your_host
  gather_facts: yes
  become: yes

  vars:
    custom_supervisor_config: "path/to/your/supervisor_config.conf"
    custom_process_config:
      - filename: "your_process_config_filename.conf"
        src: "path/to/your/process_config/"
      - filename: "app.conf"
        src: "/home/user/"

  roles:
    - ansible-role-supervisor

```

License
-------

MIT
