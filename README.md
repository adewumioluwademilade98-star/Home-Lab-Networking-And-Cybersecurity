# Home Lab Network Troubleshooting

## Overview

This project documents troubleshooting a home lab network consisting of a Bell internet gateway, a TP-Link TL-R470T+ router, a TP-Link TL-SG108E Gigabit switch, and an Intel NUC running Windows 11 Pro.

**Objective:** Establish reliable network connectivity while preserving the existing internet configuration.

## Initial Problem

I connected the TL-SG108E switch to the TL-R470T+ router and connected the Intel NUC to the switch using Ethernet.

Initially:
- The NUC could not access the internet through the switch.
- I could not access the router's administration page through that connection.

## Troubleshooting Process

### 1. Isolated the network connection

I connected the NUC directly to the TP-Link router using Ethernet. This allowed me to access the router's administration interface.

### 2. Inspected the router configuration

I reviewed the WAN, LAN, and DHCP settings without intentionally changing the configuration.

The router reported:
- WAN connection type: Dynamic IP
- WAN status: Connected
- LAN DHCP server: Enabled

Actual IP addresses and other identifying network details are intentionally omitted.

### 3. Reconnected through the switch

I reconnected the NUC through the TL-SG108E switch. Network connectivity subsequently began working.

The exact cause of the initial failure was not conclusively identified.

### 4. Verified connectivity

I used Windows networking commands to investigate the connection:

- `ipconfig` — inspected IP configuration.
- `ping` — tested network reachability.
- `nslookup` — checked DNS resolution.

The NUC subsequently obtained an address on the lab network. A test to an external IP address succeeded, DNS resolution returned an answer, and a website loaded successfully.

Specific IP addresses, MAC addresses, and network identifiers are omitted for privacy.

## Outcome

The NUC successfully accessed internet resources through the TP-Link router and switch without requiring changes to the existing Bell gateway configuration.

The original cause was not confirmed, so no specific switch or router fault is claimed.

## Skills Demonstrated

- Network troubleshooting and fault isolation
- Router administration and configuration inspection
- IPv4 addressing and subnetting
- DHCP and default gateway concepts
- Connectivity testing with `ping`
- DNS troubleshooting with `nslookup`
- Technical documentation and evidence-based reporting

## Security Considerations

This public documentation excludes:
- Router administration credentials
- Wi-Fi passwords
- Public IP addresses
- MAC addresses and device serial numbers
- Sensitive account and cloud identifiers

