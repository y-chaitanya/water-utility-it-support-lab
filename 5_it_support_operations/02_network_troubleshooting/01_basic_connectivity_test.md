# Basic Network Connectivity Test

**Status:** Completed  
**Date:** October 31, 2026  
**Environment:** macOS Terminal

## 1. Objective

Verify basic network connectivity by sending ICMP echo requests to `google.com` using the `ping` command.

## 2. Command Executed

```bash
ping -c 4 google.com
```

## 3. Actual Test Results

- Hostname: `google.com`
- Resolved IP address: `108.177.122.138`
- Packets transmitted: 4
- Packets received: 4
- Packet loss: 0%
- Minimum round-trip time: 60.323 ms
- Average round-trip time: 66.662 ms
- Maximum round-trip time: 79.513 ms

## 4. Observations

1. The hostname successfully resolved to an IP address.
2. All four ICMP echo requests received replies.
3. No packet loss was observed during this test.
4. Response times varied between approximately 60 and 80 milliseconds.

## 5. Conclusion

The test confirmed successful basic network connectivity from the Mac to the resolved Google IP address at the time of testing.

This test demonstrates basic use of the `ping` command and interpretation of packet transmission, packet loss, and round-trip response times.

## 6. Limitations

This was a basic connectivity test to an external hostname. It does not verify connectivity to internal network resources, application services, or all network devices.