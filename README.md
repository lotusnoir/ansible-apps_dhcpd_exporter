# Ansible Role: ansible-apps_squid_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_squid_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_squid_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__squid_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_squid_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_squid_exporter/tags)

Deploy [squid_exporter](https://github.com/boynux/squid-exporter) to expose squid metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `squid_exporter_version` | 1.9.1 | squid_exporter version |
| `squid_exporter_squid_host` | localhost | hostname or ip of the squid server |
| `squid_exporter_squid_port` | 3128 | port of the squid service on the squid server |
| `squid_exporter_listen_port` | 9103 | port to expose prometheus metrics |

## Examples

	---
	- hosts: apps_squid_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_squid_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
