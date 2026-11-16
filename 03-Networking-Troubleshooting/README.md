# Networking Troubleshooting Lab

## Project Overview

This project demonstrates practical networking troubleshooting skills performed in a Windows 11 virtual machine using Oracle VirtualBox.

The exercises focus on IP configuration, network connectivity, DNS resolution, DHCP lease management, firewall inspection, and connectivity diagnostics.

## Lab Environment

- Virtualization: Oracle VirtualBox
- Operating System: Windows 11 Home
- Network Mode: VirtualBox NAT
- Purpose: Practice networking troubleshooting commonly performed in Help Desk and IT Support environments.

## Tasks Completed

### 1. Network Configuration

- Inspected network adapter configuration.
- Used "ipconfig /all" to review IPv4 addressing, subnet mask, default gateway, DHCP, and DNS settings.
- Verified the VM received its network configuration through DHCP.

### 2. Network Connectivity Testing

- Used "ping" to test connectivity to the default gateway.
- Tested external IP connectivity using "8.8.8.8".
- Successfully received replies from both destinations.

### 3. DNS Troubleshooting

- Used "nslookup google.com" to verify DNS resolution.
- Identified the configured DNS server and resolved IP addresses.
- Used "ipconfig /flushdns" to clear the DNS resolver cache.

### 4. Network Route Diagnostics

- Used "tracert google.com" to inspect the route to an external destination.
- Identified the VirtualBox NAT gateway as the first hop.
- Observed that some intermediate hops did not respond to traceroute probes, while the destination responded.

### 5. DHCP Troubleshooting

- Released the existing IP configuration using "ipconfig /release".
- Requested a new configuration using "ipconfig /renew".
- Verified that the VM successfully received an IP address again.

### 6. Windows Firewall Inspection

- Inspected Windows Defender Firewall with Advanced Security.
- Reviewed Domain, Private, and Public firewall profiles.
- Verified that all three profiles were enabled.

### 7. Network Adapter Diagnostics

- Inspected the network adapter through Device Manager.
- Verified that no warning symbols were present.

### 8. HTTPS Connectivity Testing

- Used PowerShell "Test-NetConnection" to test connectivity to Google on TCP port 443.
- Confirmed "TcpTestSucceeded : True".

### 9. Final Network Verification

- Rechecked IP configuration.
- Verified gateway connectivity.
- Verified external IP connectivity.
- Confirmed DNS resolution.

## Screenshots

Screenshots documenting the completed exercises are available in the "screenshots folder" (screenshots/).

## Skills Practiced

- TCP/IP fundamentals
- IPv4 configuration
- DHCP troubleshooting
- DNS troubleshooting
- Network connectivity testing
- Traceroute diagnostics
- Windows Defender Firewall
- Device Manager
- PowerShell networking commands
- Network troubleshooting methodology
