# Ticket 003 - Windows Network Troubleshooting

## Issue

Simulated a Help Desk request involving a Windows computer experiencing possible internet connectivity problems.

The goal was to check the network configuration, test connectivity to the local gateway and internet, and verify that DNS was working correctly.

## Environment

- Windows 11 Pro ARM
- UTM virtual machine
- Command Prompt
- Microsoft Edge
- NAT virtual networking

## Troubleshooting Steps

1. Opened Command Prompt and ran `ipconfig` to check the computer's IP configuration.
2. Identified the IPv4 address as `192.168.64.2` and default gateway as `192.168.64.1`.
3. Ran `ping 192.168.64.1` to test connectivity to the default gateway.
4. Ran `ping 8.8.8.8` to test external network connectivity.
5. Ran `nslookup google.com` to verify DNS resolution.
6. Opened Google in Microsoft Edge to confirm web access.
7. Ran `tracert -d 8.8.8.8` to examine the network path to an external destination.

## Results

| Test | Result |
|---|---|
| IP configuration | 192.168.64.2 |
| Default gateway | 192.168.64.1 |
| Gateway ping | Successful |
| External ping | Successful |
| DNS lookup | Successful |
| Browser connectivity | Successful |
| Traceroute | Destination reached |

## Findings

The computer had a valid IP configuration and could communicate with its default gateway.

External ping tests and DNS resolution were successful. Microsoft Edge was also able to load websites.

Some intermediate traceroute hops did not respond, but the destination was reached. This did not indicate a confirmed connectivity failure.

No active network issue was reproduced during testing.

## Resolution

Completed network diagnostics and confirmed that local connectivity, external connectivity, DNS, and web browsing were functioning.

No network configuration changes were required.

Status: Closed - No Fault Found

## Skills Used

- TCP/IP networking
- Windows Command Prompt
- IP configuration
- Ping testing
- DNS troubleshooting
- Traceroute
- Network troubleshooting
- Technical documentation

## Notes

This was a simulated Help Desk scenario completed in my Windows 11 home lab. No actual customer incident or production network was involved.