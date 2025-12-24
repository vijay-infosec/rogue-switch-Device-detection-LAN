This folder contains outputs showing MAC flooding activity forwarded through the rogue switch uplink and the resulting port-security response.

## Files
- cam_after_mac_flooding.png — Large number of MAC addresses learned on Gi0/0.
- port_security_sticky.png — Sticky MAC configured on the uplink.
- port_security_violation_log.png — Port-security violations triggered by spoofed MACs.
- port_security_status_after_attack.png — Interface placed into secure-shutdown with high violation count.

## Summary
The switch detects excessive MAC learning on the uplink, triggers port-security violations, and shuts down the interface, preventing CAM table exhaustion caused by flooding behind the rogue switch.
