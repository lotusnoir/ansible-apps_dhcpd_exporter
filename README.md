# Ansible Role: ansible-apps_dhcpd_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_dhcpd_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_dhcpd_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_dhcpd_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_dhcpd_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_dhcpd_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_dhcpd_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_dhcpd_exporter.svg)](https://github.com/lotusnoir/ansible-apps_dhcpd_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_dhcpd_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_dhcpd_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_dhcpd_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_dhcpd_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_dhcpd_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_dhcpd_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_dhcpd_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_dhcpd_exporter)

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
