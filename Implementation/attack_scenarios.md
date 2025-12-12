# Attack Scenarios (Rogue Switch as the Enabler, Not the Attacker)

A rogue switch is an unauthorized extension of the LAN that allows attackers to bypass port-level controls and hide multiple devices behind a single uplink. 
The attacks originate from the device connected behind the rogue switch, but the switch enables them to propagate deeper into the network.

---

### 1. ARP Spoofing via Rogue Switch Uplink
The downstream attacker uses the rogue switch to inject forged ARP replies. 
Because multiple devices sit behind one port, the legitimate switch cannot enforce normal per-port security.

Key observations:
- Unsolicited ARP replies entering through the rogue switch uplink  
- Gateway and host MAC entries overwritten  
- Traffic redirected through the attacker behind the switch  

---

### 2. STP Manipulation by Unauthorized Switch
Only a switch can send BPDUs. 
The attacker introduces a rogue switch configured to send superior BPDUs, attempting to reposition itself within the spanning-tree topology.

Key observations:
- Superior BPDUs arriving from an unauthorized switch  
- Sudden changes in root ID or priority  
- Uplink entering root-inconsistent state (Root Guard trigger)  

---

### 3. MAC Flooding Generated Behind the Rogue Switch
The attacker floods the network with fabricated MAC addresses through the rogue switch. 
The switch amplifies the attack by funneling many addresses into a single uplink.

Key observations:
- Excessive MAC learning on one interface  
- CAM table saturation  
- Switch fallback to broadcast behavior  
