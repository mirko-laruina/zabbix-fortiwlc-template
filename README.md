# zabbix-fortiwlc-template
Zabbix template for FortiWLC controller (with APs) monitoring

It monitors the following infos from the controller:
- CPU
- memory
- disk space
- uptime
- name
- model
- version
- online APs
- RX/TX throughput
- total number of alarms

For each AP, it collects:
- availability
- alarm state
- operational state
- uptime
- boot and runtime version
- positioning info (building, floor, location, contact)
- hardware info (MAC address, HW rev, HW type)
- vlan name
- ip address

Zabbix problems are triggered if
- AP has an active alarm
- AP is not available
- operational state is different from "online"
- AP IP address has changed
- AP has rebooted (uptime decreased)
