# Detection Rules (Focused on Rogue Switch Exposure)

The detection rules target behaviours that indicate an unauthorized switch has extended the LAN and is enabling downstream attacker activity.

---

### Rule 1 – Unauthorized Switch Topology Behaviour
Detect switches attempting to join or influence LAN topology.

Key indicators:
- Superior BPDUs on an unexpected port  
- Sudden changes in root bridge identity  
- Port transitioning to root-inconsistent state  

---

### Rule 2 – Uplink Anomalies Suggesting Hidden Devices
Identify multiple or unknown devices appearing behind a single interface (typical sign of a rogue switch).

Key indicators:
- Multiple MAC–IP mappings behind one access port  
- Unknown MAC addresses not present in baseline  
- Devices appearing on unexpected VLANs or ports  

---

### Rule 3 – ARP Manipulation Originating Through the Rogue Switch
Detect ARP tampering activity sent by the attacker but funneled through the rogue switch uplink.

Key indicators:
- Unsolicited ARP replies  
- Duplicate IP usage  
- Rapid ARP table flips associated with one interface  
