# Ticket 001 - Windows Performance Troubleshooting

## Issue

Simulated a Help Desk request involving a Windows computer running slowly while using a web browser.

The goal was to check system performance, identify which applications were using the most memory, and determine whether closing those applications improved resource usage.

## Environment

- Windows 11 Pro ARM
- UTM virtual machine
- Apple Silicon MacBook
- 8 GB RAM allocated to Windows
- Windows Task Manager
- Microsoft Edge

## Troubleshooting Steps

1. Opened Task Manager to check CPU and memory usage.
2. Recorded the initial memory usage at approximately 3.1 GB.
3. Opened multiple Microsoft Edge tabs to increase memory usage.
4. Monitored Task Manager to identify which processes were consuming the most resources.
5. Observed Microsoft Edge using approximately 1,915 MB of memory.
6. Closed Edge and checked memory usage again.
7. Compared the results to determine how much memory was released.

## Results

| Test | Memory Usage |
|---|---|
| Before opening Edge | 3.1 GB |
| During browser testing | 5.44 GB (68%) |
| Microsoft Edge process | 1,915 MB |
| After closing Edge | 4.6 GB |

## Findings

Memory usage increased while multiple browser tabs were open. Microsoft Edge was one of the largest memory-consuming applications during testing.

After closing Edge, overall memory usage decreased from approximately 5.44 GB to 4.6 GB.

This showed that browser activity contributed to higher memory consumption. No underlying Windows or hardware issue was confirmed.

## Resolution

Closed the browser workload and verified that memory usage decreased.

No additional changes were needed for this simulated troubleshooting exercise.

Status: Closed - Investigation Completed

## Skills Used

- Windows Task Manager
- Performance troubleshooting
- CPU and RAM monitoring
- Application troubleshooting
- Technical documentation

## Notes

This was a simulated Help Desk scenario completed in my Windows 11 home lab. No actual customer incident was involved.