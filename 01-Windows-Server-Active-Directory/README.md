# Windows Server 2025 & Active Directory Lab

## Project Overview

This project demonstrates hands-on experience deploying and managing a Windows Server 2025 environment using Oracle VirtualBox. The lab focuses on Active Directory administration, DNS, DHCP, and Windows 11 client networking.

The objective was to practice common IT support and junior systems administration tasks in a virtualized environment.

## Lab Environment

Component| Configuration
Hypervisor| Oracle VirtualBox
Server OS| Windows Server 2025 Standard Evaluation
Client OS| Windows 11
Domain| corp.example.com
NetBIOS Name| CORP
Server Hostname| ITLAB-SERVER

## 1. Active Directory Domain Services

Configured and verified Active Directory Domain Services (AD DS).

Tasks performed:

- Verified domain configuration.
- Inspected Active Directory organizational units.
- Retrieved and reviewed domain user accounts.
- Created and managed a custom domain user account.
- Enabled and disabled user accounts using PowerShell.

PowerShell commands used:

Get-ADDomain

Get-ADOrganizationalUnit -Filter *

Get-ADUser -Filter * -Properties Enabled

## 2. User and Security Group Management

Practiced common Active Directory account administration tasks.

Tasks performed:

- Reviewed existing domain user accounts.
- Disabled and re-enabled a user account.
- Created a custom global security group named HelpDesk_Tier1.
- Added a domain user to the security group.
- Verified group membership.

PowerShell commands used:

Disable-ADAccount -Identity "John Smith"

Enable-ADAccount -Identity "John Smith"

New-ADGroup -Name "HelpDesk_Tier1" -GroupScope Global -GroupCategory Security -Path "CN=Users,DC=corp,DC=example,DC=com"

Add-ADGroupMember -Identity "HelpDesk_Tier1" -Members "John Smith"

Get-ADGroupMember -Identity "HelpDesk_Tier1"

## 3. DNS Configuration

Verified the DNS Server role and inspected DNS zones and records.

Tasks performed:

- Verified DNS Server role installation.
- Inspected DNS zones.
- Reviewed DNS resource records.
- Tested domain and server hostname resolution from Windows 11.

PowerShell and command-line tools:

Get-WindowsFeature DNS

Get-DnsServerZone

Get-DnsServerResourceRecord -ZoneName "corp.example.com"

Windows 11 tests:

nslookup corp.example.com

nslookup ITLAB-SERVER

## 4. DHCP Configuration

Inspected and verified DHCP Server configuration.

Tasks performed:

- Verified DHCP Server role installation.
- Reviewed IPv4 DHCP scopes.
- Inspected DHCP leases.
- Reviewed configured DHCP scope options.

PowerShell commands used:

Get-WindowsFeature DHCP

Get-DhcpServerv4Scope

Get-DhcpServerv4Lease -ScopeId <ScopeId>

Get-DhcpServerv4OptionValue -ScopeId <ScopeId>

## 5. Windows 11 Client Networking

Used a Windows 11 virtual machine to test connectivity and network configuration.

Tasks performed:

- Tested connectivity to the Windows Server machine.
- Verified DNS name resolution.
- Inspected IPv4 network configuration.
- Reviewed DNS server and gateway settings.

Command-line tools used:

ping ITLAB-SERVER

ipconfig /all

nslookup corp.example.com

## 6. Technologies and Tools

- Windows Server 2025
- Windows 11
- Active Directory Domain Services
- DNS
- DHCP
- Oracle VirtualBox
- PowerShell
- Command Prompt
- TCP/IP
- IPv4
- DNS name resolution

## 7. Skills Practiced

- Active Directory administration
- Domain user account management
- Security group administration
- DNS configuration and troubleshooting
- DHCP scope and lease management
- Windows client network troubleshooting
- PowerShell administration
- Virtual machine management

## 8. Project Screenshots

Screenshots documenting the lab configuration and testing are available in the "screenshots folder" (screenshots/).

The evidence includes domain verification, Active Directory administration, security group management, DNS configuration, DHCP configuration, and Windows 11 connectivity tests.

---

Project Status: Completed

Environment: Personal virtualized home lab

Documentation: Hands-on configuration and testing evidence included. 
