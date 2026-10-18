SUPPORT TICKET #001 — Browser Memory Utilization Investigation
Category: Desktop Support / Performance
Environment: Windows 11 Pro running in UTM
Priority: Low — Training
Type: Simulated Support Case

Issue Description:
Investigated the effect of multiple Microsoft Edge browser tabs on Windows 11 memory utilization in a controlled virtual lab.

Troubleshooting Steps:
1. Established baseline resource utilization using Task Manager.
2. Opened multiple Microsoft Edge tabs to simulate a browser workload.
3. Monitored RAM consumption and browser process memory.
4. Closed Edge and measured total memory utilization afterward.
5. Compared baseline, workload, and recovery readings.

Findings:
Baseline RAM: 3.1 GB
Peak observed RAM: approximately 5.44 GB (68%)
Edge memory: 1,915 MB
Available memory with Edge open: 2.8 GB
RAM after closing Edge: 4.6 GB
Observed reduction: approximately 0.84 GB

Conclusion:
Memory utilization increased during browser activity and decreased after Edge was closed. No memory exhaustion or confirmed software fault was identified.

Verification:
Task Manager showed reduced total RAM consumption after closing the browser.