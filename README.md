# alaxala-ax24s-zabbix-template
AlaxalA Switch AX2400S series monitoring Zabbix template 

## Description
This is AlaxalA AX2400S series Switch monitoring Zabbix template using SNMP.
This template based on [mib2zabbix](https://github.com/cavaliercoder/mib2zabbix).

This template is checked on following environment:
- Zabbix Server 5.2
- AX2430S-48T, AX2430S-48T2X
- SNMPv1
  - not checked SNMPv2/v3.

## Usage
**Before using this template, set snmp config on AlaxalA Switch (probability default is off).**
Import this template and link this template to AlaxalA switch host config.
If create AlaxalA host using this template,
- interface is set `SNMP`
- If many snmp error is occured, `using bulk request` set DISABLED (this is recomended).
  - Sometimes, this option `using bulk request` causes many SNMP errors(ex: general error/network error/etc...) and drop SNMP request.

## TODO(Feature Work)
- change item names (now: SNMP key name from MIB)
- create trigger, graph and screen prototype
- check snmptrap item (now: default disabled and no check)
- check all items and delete some item if need not.

## Author
author: hinananoha
