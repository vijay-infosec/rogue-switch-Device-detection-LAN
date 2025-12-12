# STP Manipulation Detection (Root Guard Against Rogue Switch)

A rogue switch can send superior BPDUs to alter the spanning-tree topology. This is the only attack where the rogue switch itself generates malicious protocol frames.

## Indicators Linked to Rogue Switch Activity
- Superior BPDUs arriving on unauthorized ports  
- Unexpected root MAC/priority transitions  
- Uplink entering root-inconsistent state  

## Mitigation
- Enable Root Guard on all access-facing uplinks  
- Audit STP role changes and BPDU sources  
- Monitor for repeated root-inconsistent triggers  
