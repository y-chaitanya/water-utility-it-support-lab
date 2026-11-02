# Network Interface, Routing, DNS, and VPN Configuration Inspection

## Objective
Inspect the Mac's network interfaces, default route, configured VPN services, and DNS resolver settings. Verify DNS resolution using `dig`.

## Environment
- Operating system: macOS
- Network interface: en0
- Network type: Local network connection
- Target hostname: google.com

## Commands Performed
- `ifconfig` — inspected network interfaces and IP configuration.
- `route -n get default` — identified the default gateway and outgoing interface.
- `scutil --nc list` — checked configured network connection services.
- `scutil --dns` — inspected DNS resolver configuration.
- `dig google.com` — tested DNS resolution and reviewed the response.

## Findings

### 1. Network Interface Configuration
- Active primary interface: `en0`
- IPv4 address: `192.168.1.64`
- Subnet mask: `255.255.255.0`
- Broadcast address: `192.168.1.255`
- MTU: `1500`
- Several `utun` point-to-point tunnel interfaces were present.

The presence of `utun` interfaces alone does not establish that a VPN connection is active.

### 2. Default Route
The default route was configured through:
- Gateway: `192.168.1.254`
- Interface: `en0`
- Route status: `UP`

This gateway matched the first responding hop in the earlier traceroute exercise.

### 3. VPN Service Inspection
`scutil --nc list` did not display any configured network connection services.

This output does not rule out VPN software or network tunnels implemented through other macOS mechanisms. No active VPN connection was independently verified during this exercise.

### 4. DNS Resolver Configuration
The primary resolver configuration showed:
- IPv4 DNS server: `192.168.1.254`
- IPv6 DNS server: `2600:1700:7ac0:a0f0::1`
- Search domain: `attlocal.net`
- Primary interface: `en0`

The primary resolver was reported as reachable.

### 5. DNS Query Verification
Command: `dig google.com`

Results:
- Query status: `NOERROR`
- Query type: `A` (IPv4 address lookup)
- Answer records: 6 IPv4 addresses
- DNS server used: `2600:1700:7ac0:a0f0::1`
- Query time: `17 ms`

The query successfully returned IPv4 address records for `google.com`.

## Troubleshooting Observations
- The primary network interface had an IPv4 address and an active default route.
- The default gateway was consistent with the first hop reported by traceroute.
- The configured DNS resolver was reachable.
- DNS resolution completed successfully with a `NOERROR` response.
- Tunnel interfaces were present, but their presence alone was not sufficient to confirm an active VPN.
- No configured VPN services appeared in the `scutil --nc list` output.

## Conclusion
The inspection confirmed that the Mac had an active network interface, a configured default route, and a reachable DNS resolver. The `dig` test successfully resolved `google.com`.

No DNS resolution failure was observed during this exercise. VPN connectivity was not tested, so no conclusion about an active VPN connection can be made.

## Scope and Limitations
This was a hands-on macOS network configuration inspection in a personal environment. It was not performed on a corporate network, managed endpoint, or production VPN. No network settings were changed.

## Status
Completed — macOS network configuration and DNS inspection.
