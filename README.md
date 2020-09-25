# Ansible Role: ansible-apps_dhcpd_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_dhcpd_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_dhcpd_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__dhcpd_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_dhcpd_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_dhcpd_exporter/tags)

Deploy [dhcpd_exporter](https://github.com/lotusnoir/prometheus-dhcpd_exporter) to expose dhcpd metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `dhcpd_exporter_listen` | 0.0.0.0 | listen address |
| `dhcpd_exporter_port` | 9119 | port to expose prometheus metrics |

## Examples

	---
	- hosts: apps_dhcpd_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_dhcpd_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
