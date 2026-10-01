# CMPG325 Troubleshooting Record

## Purpose

This document records troubleshooting activities encountered during the implementation and testing of the Ramokoka & Partners Attorneys network in Cisco Packet Tracer. The record documents the observed issue, diagnostic approach, resolution or workaround, and supporting evidence.

## 1. ACL Interface Status Display

### Observed Issue

During verification of the public Wi-Fi ACL on VLAN 50, the command `show ip interface vlan 50` displayed:

`Inbound access list is not set`

This appeared inconsistent with the VLAN 50 running configuration, which contained the ACL application command.

### Investigation

The ACL was first verified using `show access-lists PUBLIC_WIFI_FILTER`, confirming that the ACL existed. The VLAN 50 configuration was then inspected using `show running-config`, where the following configuration was found:

`ip access-group PUBLIC_WIFI_FILTER in`

The command `show running-config | include access-group` was also used to confirm that the ACL application command was present.

### Verification

The ACL was subsequently tested from the public Wi-Fi network. Traffic to the protected internal VLANs generated matches on the deny rules, while permitted traffic generated matches on the final permit rule.

### Outcome

The ACL filtering policy was verified through its actual traffic behaviour and ACL match counters.

**Evidence:**
- `28_ACL_Interface_Status_Diagnostic.png`
- `29_VLAN50_ACL_Configuration.png`
- `30_ACL_Access_Group_Verification.png`
- `26_PUBLIC_WIFI_ACL_Deny_Matches.png`
- `27_PUBLIC_WIFI_ACL_Permit_Match.png`

---

## 2. Unsupported Interface Configuration Command

### Observed Issue

The command:

`show running-config interface vlan 50`

was attempted to inspect the VLAN 50 configuration. Cisco Packet Tracer returned an invalid-input message.

### Investigation

The command was not supported by the IOS implementation available in the Packet Tracer device.

### Resolution

The full running configuration was inspected using:

`show running-config`

The `interface Vlan50` section was then located manually. The ACL application command was confirmed in that section.

### Outcome

The required configuration was successfully verified using a supported Packet Tracer command.

**Evidence:**
- `31_Unsupported_CLI_Command.png`
- `29_VLAN50_ACL_Configuration.png`

---

## 3. Public Wi-Fi ACL Traffic Testing

### Observed Issue

Connectivity from the public Wi-Fi network to protected internal network segments was tested after implementing the ACL.

### Investigation

GUEST-LT01 was used to test connectivity to addresses within the Attorneys, Support/Admin, Reception, Shared Services and Management VLANs.

The tests returned destination-unreachable responses, and the ACL counters subsequently showed four matches on each corresponding deny rule.

### Outcome

The testing confirmed that public Wi-Fi traffic to the protected internal VLANs was being filtered according to the configured ACL policy.

Traffic to the routed R1 address outside the protected VLAN ranges was permitted, and the final permit rule recorded four matches.

**Evidence:**
- `26_PUBLIC_WIFI_ACL_Deny_Matches.png`
- `27_PUBLIC_WIFI_ACL_Permit_Match.png`
