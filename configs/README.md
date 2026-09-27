# Sanitised Configuration Exports

These files preserve the supplied configurations for R3, S2 and ASA1. They are documentation snapshots, not a complete or ready-to-import lab deployment.

## Privacy changes

- Local account names are replaced with `<REDACTED_USERNAME>`.
- Passwords, secret hashes and NTP authentication key values are replaced with `<REDACTED>`.
- The configured domain is replaced with `lab.example`.
- Device serial/UDI information is omitted.
- Learned sticky MAC addresses are replaced with `<REDACTED_MAC>`.
- Device labels, lab IP addresses, interfaces, routes and security policies are retained.

The retained password encoding markers describe the original command syntax; the placeholders are not valid encoded credentials. Configure your own local lab credentials and learn your own device MAC addresses before use. These exports do not include the Packet Tracer activity file.

## What these exports show

| Device | Visible configuration |
| --- | --- |
| R3 | Local AAA, SSH v2, zone-based firewall, default routing, syslog and authenticated NTP |
| S2 | Port security with a two-address limit and protect mode, sticky MAC learning, PortFast and BPDU Guard on FastEthernet0/18 |
| ASA1 | Inside/outside interfaces, dynamic PAT, default route, local SSH authentication, DHCP and ICMP inspection |

R3 includes an IPS configuration storage location, but this export alone does not demonstrate a complete active IPS policy. VLAN segmentation, trunking and DHCP snooping are part of the broader README scope but are not demonstrated by the supplied S2 export. Other device configurations and test results can be added to document the remaining lab scope.
