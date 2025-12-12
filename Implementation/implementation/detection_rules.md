# Detection Rules (Rogue Switch–Enabled Indicators)

Detection focuses on behaviours that reveal the presence of an unauthorized switch extending the LAN and enabling downstream attacker activity.

---

## Rule 1 – Topology Behaviour of Unauthorized Switches
Identify rogue switches attempting to integrate into STP or alter topology.

### Indicators Linked to Rogue Switch Activity
- Superior BPDUs received on non-root-facing ports  
- Sudden changes in root ID or priority  
- Ports entering root-inconsistent state  

---

## Rule 2 – Uplink Patterns Showing Hidden Devices
Detect multiple or unknown devices appearing behind a single port, consistent with a rogue switch.

### Indicators Linked to Rogue Switch Activity
- Multiple MAC–IP bindings on one interface  
- Unknown MAC addresses absent in baseline  
- Endpoints appearing on unexpected VLANs or ports  

---

## Rule 3 – ARP Manipulation Through Rogue Switch Path
Detect ARP spoofing performed by the attacker but funneled through the rogue switch uplink.

### Indicators Linked to Rogue Switch Activity
- Unsolicited ARP replies inbound through one interface  
- Duplicate IP usage detected from the same uplink  
- Rapid ARP table changes tied to one port  
