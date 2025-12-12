# Attack Scenarios (Rogue Switch–Centric)

The primary threat in this project is the introduction of a **rogue switch** into the LAN.  
The rogue device is only an endpoint attached behind the rogue switch; all malicious activity originates from the switch’s unauthorized extension of the network fabric.

---

### 1. Rogue Switch Enabling ARP Spoofing
The rogue switch extends the LAN to unauthorized devices, allowing a downstream attacker to inject forged ARP replies.  
The switch’s uplink masks multiple hosts behind a single port, bypassing port-level controls.

Key behaviours:
- Unsolicited ARP replies reaching multiple hosts  
- Gateway MAC overwritten across the network  
- Traffic interception via the rogue switch uplink  

---

### 2. Rogue Switch Manipulating STP (Root Takeover Attempt)
Only a rogue **switch**—not a device—can send BPDUs capable of influencing Spanning Tree Protocol.  
The rogue switch attempts to become the root bridge, placing itself in the forwarding path.

Key behaviours:
- Superior BPDUs from unauthorized bridge  
- Unexpected root ID and root MAC changes  
- Uplink ports entering root-inconsistent state  

---

### 3. Rogue Switch Executing MAC Flooding
The rogue switch forwards high-volume spoofed MAC traffic from its downstream p
