# Templates-Zabbix-Huawei

- Pay attention at discovery FILTERS os all templates.
- BGP Template only for IPv4 Peers/Neighbors. (Not able to implement v6 yet) If you do this based on my Template please share me by sending via gustavoifelippe@hotmail.com
- If you need any files that's not included here, please be in touch by gustavoifelippe@hotmail.com, and I'll help you in my time.
- Using traps via SNMPTT and SNMPTRAPDEAMON.
- Configuration on BGP routers for the traps:
    - snmp-agent trap enable
    - undo snmp-agent trap enable feature-name bgp trap-name bgpBackwardTransNotification
    - undo snmp-agent trap enable feature-name bgp trap-name bgpEstablishedNotification
- If you are using s6730, please put the following configuration:
    - "set if-mib sample-interval 0"

Zabbix Version 4.0.17
