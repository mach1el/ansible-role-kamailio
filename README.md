# Ansible Role for Kamailio
![Version](https://img.shields.io/github/v/tag/mach1el/ansible-role-kamailio?color=magenta&label=Ver&style=flat-square) ![License](https://img.shields.io/github/license/mach1el/ansible-role-k)

Auto build,deploy kamailio with ansible.

## Role variables
See [`default/main.yml`](https://github.com/mach1el/ansible-role-kamailio/blob/master/defaults/main.yml)

You may need to change/specify some variables below.

* `kamailio_db_engine`
* `kamailio_db_root_pass`
* `kamailio_db_connect_engine`

## Role pathes

	├── defaults
	│   └── main.yml
	├── handlers
	│   └── main.yml
	├── tasks
	│   ├── main.yml
	│   └── setup_debian.yml
	└── templates
		├── config
		│   ├── kamailio.cfg.j2
		│   └── kamctlrc.j2
		└── pgpass


## Example playbook
	---
	- name: Building kamailio for local server
		hosts: local_server
		become: true

		roles:
			- '../ansible-role-kamailio'
