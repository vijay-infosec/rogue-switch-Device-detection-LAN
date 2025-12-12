# ML-Based Detection of Rogue Switch–Enabled Traffic Patterns

The ML model classifies traffic as legitimate or rogue-enabled by analysing deviations in Layer 2 behaviour caused by unauthorized switches and downstream attackers.

## Key Features Used
- STP field anomalies (root MAC/priority shifts)  
- ARP reply timing and source patterns through one interface  
- High MAC variability associated with a single uplink  

## Output
- Binary classification (normal vs. rogue-enabled)  
- Probability score indicating abnormal Layer 2 behaviour  
