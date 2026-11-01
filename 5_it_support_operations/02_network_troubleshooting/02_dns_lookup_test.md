# DNS Lookup Test

**Status:** Completed  
**Date:** October 31, 2026  
**Environment:** macOS Terminal

## 1. Objective

Use the `nslookup` command to examine how the Domain Name System (DNS) resolves a hostname to IP addresses.

## 2. Command Executed

```bash
nslookup google.com
```

## 3. Actual Test Results

**Hostname queried:** `google.com`

**DNS server used:**
- Server address: `2600:1700:7ac0:a0f0::1`
- DNS port: `53`

**IPv4 addresses returned:**
- `108.177.122.139`
- `108.177.122.138`
- `108.177.122.101`
- `108.177.122.100`
- `108.177.122.113`
- `108.177.122.102`

**Response type:** Non-authoritative answer

## 4. Observations

1. The DNS lookup successfully returned IP addresses for `google.com`.
2. The DNS resolver used an IPv6 address.
3. Six IPv4 addresses were returned for the requested hostname.
4. The response was identified as non-authoritative, meaning it was provided by a DNS resolver rather than directly by an authoritative DNS server for the domain.

## 5. Conclusion

The test demonstrated successful DNS name resolution using the `nslookup` command.

It provided practical exposure to identifying the DNS resolver, understanding DNS port 53, and interpreting hostname-to-IP-address results.

## 6. Limitations

This exercise tested DNS resolution for one public hostname. It did not test internal corporate DNS, DNS record management, or DNS server administration.