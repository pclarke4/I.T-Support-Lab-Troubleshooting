# Help Desk Ticket #003 — Windows Network Connectivity Troubleshooting

**Ticket ID:** HD-003  
**Category:** Network Connectivity / Troubleshooting  
**Priority:** Medium (Simulated)  
**Environment:** Windows 11 Pro ARM, UTM Virtual Machine  
**User:** TestEmployee (Lab Account)  
**Status:** Closed — No Fault Found  
**Issue Type:** Simulated Help Desk Scenario

## 1. Problem Description

A simulated employee reported being unable to access the internet from their Windows workstation.

The objective was to diagnose the issue using Windows networking utilities, verify local and external connectivity, and identify potential DNS or routing problems.

## 2. Troubleshooting Steps

### Step 1 — Verify IP Configuration

**Command:** `ipconfig`

**Findings:**
- IPv4 Address: `192.168.64.2`
- Default Gateway (IPv4): `192.168.64.1`
- An IPv6 link-local default gateway was also present.

**Result:** Windows had a private IPv4 address and a configured default gateway.

### Step 2 — Test Default Gateway Connectivity

**Command:** `ping 192.168.64.1`

**Result:** Successful ICMP replies.

**Finding:** The virtual machine could communicate with its configured IPv4 gateway.

### Step 3 — Test External IP Connectivity

**Command:** `ping 8.8.8.8`

**Result:** Successful ICMP replies.

**Finding:** The system could reach an external public IP address.

### Step 4 — Verify DNS Resolution

**Command:** `nslookup google.com`

**Result:** DNS successfully returned IP addresses.

**Finding:** Domain-name resolution functioned for the tested domain.

### Step 5 — Verify HTTPS Website Access

**Test:** Opened `https://www.google.com` in Microsoft Edge.

**Result:** Website loaded successfully.

**Finding:** HTTPS website access was functioning for the tested site.

### Step 6 — Trace Network Route

**Command:** `tracert -d 8.8.8.8`

**Results:**
- First hop: `192.168.64.1`
- Some intermediate hops did not respond.
- Destination was successfully reached.

**Finding:** The route to the destination was completed despite intermediate probe timeouts.

## 3. Root Cause Analysis

No active network connectivity fault was reproduced during testing.

The simulated workstation demonstrated functioning IP configuration, gateway communication, external connectivity, DNS resolution, and HTTPS access.

**Root cause:** Undetermined — no fault reproduced.

## 4. Resolution

No configuration changes or repairs were necessary.

All diagnostic tests completed successfully. The simulated ticket was closed as **No Fault Found**.

## 5. Skills Demonstrated

- Windows 11 Network Troubleshooting
- TCP/IP Fundamentals
- IPv4 Addressing and Default Gateways
- ICMP Connectivity Testing
- DNS Diagnostics
- Network Route Analysis
- Command Prompt Utilities
- Structured IT Troubleshooting
- Technical Documentation

## 6. Lessons Learned

A valid IP address does not guarantee internet connectivity. Effective network troubleshooting requires testing each component systematically.

Successful gateway connectivity, external IP connectivity, DNS resolution, and HTTPS access provide stronger evidence of a functioning connection than any individual test alone.

Additionally, intermediate traceroute timeouts do not automatically indicate a network outage.