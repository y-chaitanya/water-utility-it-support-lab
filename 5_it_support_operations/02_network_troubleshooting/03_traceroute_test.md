# Traceroute Test

## Objective
Identify the network path between the local Mac system and
Google's destination server using traceroute.

## Environment
- Device: Mac
- Operating system: macOS
- Command: traceroute -m 12 google.com
- Maximum hops: 12

## Command Executed

```bash
traceroute -m 12 google.com
```

Google resolved to multiple addresses. Traceroute selected
142.250.9.102.

The destination was reached in 6 hops.

| Hop | Host / IP Address | Response Times (ms) |
|---|---|---|
| 1 | dsldevice (192.168.1.254) | 13.992, 5.310, 5.418 |
| 2 | 107.201.140.1 | 10.508, 9.293, 7.871 |
| 3 | 64.148.105.88 | 8.712, 11.711, 7.874 |
| 4 | 12.242.115.21 | 53.167, 13.056, 17.015 |
| 5 | 12.255.10.174 | 52.572, 13.143, 11.160 |
| 6 | yq-in-f102.1e100.net (142.250.9.102) | 59.057, 54.572, 54.584 |

## Observations

- The first hop identified the local network gateway.
- The destination responded at hop 6.
- All six hops returned responses.
- Response times varied across individual probes.
- The trace completed before reaching the maximum of 12 hops.

## Conclusion

The traceroute test successfully identified the network path
from the Mac to Google's destination.

## Limitations

- Results represent one test at one point in time.
- Network routes may change.
- Response times alone do not establish persistent congestion.
- This test does not establish the health of internal corporate
  networks or VPN connections.

## Status

Completed - tested on macOS.
