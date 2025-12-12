# MAC Flooding Detection Using Port Security

The attacker behind the rogue switch generates numerous spoofed MAC addresses. The rogue switch forwards all addresses into the legitimate switch, exhausting the CAM table.

## Indicators Linked to Rogue Switch Activity
- Rapid MAC table growth on a single interface  
- Frequent port-security violations  
- Port entering err-disabled due to excessive MACs  

## Mitigation
- Configure MAC learning limits  
- Enable Sticky MAC on access ports  
- Monitor violation counters for uplink saturation  
