# Templates-Zabbix-Huawei
Functionalities:
    - Optical modules signal per lane fully SNMP.
    - Network interfaces and BGP Peers/Neighbors/Sessions monitoring by SNMP Trap.
    - Resources (CPU/Memory/Temperature).
    - PPPoE access-user count summary, and separated by Single-Tagged and Double-Tagged subinterfaces.
   
OBS:   
- Pay attention at discovery FILTERS os all templates.

- If you need any files that's not included here, please be in touch by gustavoifelippe@hotmail.com, and I'll help you in my time.

- Using traps via SNMPTT and SNMPTRAPDEAMON.

- Configuration on BGP routers for the traps:
    - snmp-agent trap enable
    - undo snmp-agent trap enable feature-name bgp trap-name bgpBackwardTransNotification
    - undo snmp-agent trap enable feature-name bgp trap-name bgpEstablishedNotification

- In some Huawei switch models, you'll need to put the following configuration in order to the graphs works properly, and without any degradation:
    - "set if-mib sample-interval 0"

- In order to collect user-vlan descriptions using the BNG Template, you'll have to manually configure descriptions in your router subinterfaces by following these steps:
    - Single-tagged vlans (not QinQ):
      interface Eth-Trunk0.0
      user vlan 0
        vlan 0 description "Put the description here without quotes"
   
    - Double-tagged vlans (QinQ):
      interface Eth-Trunk0.1
      user vlan 0 qinq 1
        vlan 0 qinq 1 description "Put the description here without quotes"

      
Zabbix Version 4.0.17
