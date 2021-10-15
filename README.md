# Ansible Role: ansible-apps_dhcpd_exporter

## Description

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_dhcpd_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_dhcpd_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_dhcpd_exporter.svg)](https://github.com/lotusnoir/ansible-apps_dhcpd_exporter/releases/latest)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_dhcpd_exporter?color=orange&style=flat)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_dhcpd_exporter)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)


Deploy [dhcpd_exporter](https://github.com/atonkyra/dhcp-stats-prometheus) to expose dhcpd metrics to prometheus.

## Role variables

| Name                         | Default Value  | Description                        |
| ---------------------------- | -------------- | -----------------------------------|
| `dhcpd_exporter_listen`      | 0.0.0.0        | listen address |
| `dhcpd_exporter_port`        | 9119           | port to expose prometheus metrics |
| `dhcpd_exporter_install_dir` | /usr/local/bin | Install directory for binary |

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

## Prometheus rules

TODO

## Grafana dashboard

A sample dashboard is available here: [https://grafana.com/grafana/dashboards/13589](https://grafana.com/grafana/dashboards/13589)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
