# ARP Spoofing Detection Using DAI (Rogue Switch Context)

The attacker injects forged ARP replies through the rogue switch uplink. Dynamic ARP Inspection (DAI) validates ARP traffic against DHCP snooping bindings and blocks mismatches.

## Indicators Linked to Rogue Switch Activity
- DAI logs showing repeated invalid ARP packets on one port  
- MAC or IP inconsistencies traced to the uplink  
- Continuous ARP Opcode 2 (reply) traffic without requests  

## Mitigation
- Enable DAI on relevant VLANs  
- Maintain accurate DHCP snooping bindings  
- Monitor DAI violation counters for uplink anomalies  
