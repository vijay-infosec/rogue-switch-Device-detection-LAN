This folder contains screenshots showing how the rogue switch attempted to become the STP root and how Root Guard blocked the manipulation.

## Indicators Observed
- Unexpected root ID and priority values after attack
- Superior BPDUs received from unauthorized switch
- Root Guard logs:
  - ROOTGUARD_CONFIG_CHANGE
  - ROOTGUARD_BLOCK
- Interface marked as "Root Inconsistent"

These outputs confirm successful detection and containment of the rogue switch.
