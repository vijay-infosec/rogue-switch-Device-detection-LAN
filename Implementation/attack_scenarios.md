# Attack Scenarios (Rogue Switch as Enabler, Not Attacker)

A rogue switch is an unauthorized extension of the LAN. It allows multiple downstream devices to enter the network through a single uplink, bypassing port-level controls. The malicious activity originates from the attacker’s device behind the rogue switch, while the switch enables that activity to propagate.

---

## 1. ARP Spoofing via Rogue Switch Path
The attacker uses the rogue switch uplink to inject forged ARP replies. The switch masks the attacker by forwarding all traffic through one interface.

### Indicators Linked to Rogue Switch Activity
- Unsolicited ARP replies inbound on the same uplink  
- IP–MAC inconsistencies associated with one interface  
- DAI violation logs repeatedly triggered by uplink traffic  

---

## 2. STP Manipulation by Unauthorized Switch
The rogue switch participates in STP and sends superior BPDUs to influence the network topology. This is the only attack where the switch itself generates malicious control traffic.

### Indicators Linked to Rogue Switch Activity
- Superior BPDUs arriving from an unexpected switch  
- Root MAC or priority changing unexpectedly  
- Port entering root-inconsistent state (Root Guard activation)  

---

## 3. MAC Flooding Triggered Behind the Rogue Switch
The attacker behind the switch generates a large number of spoofed MAC addresses. The rogue switch forwards them into the legitimate switch, overwhelming its CAM table.

### Indicators Linked to Rogue Switch Activity
- Excessive MAC learning on a single interface  
- CAM table saturation  
- Port security violations tied to the uplink  
