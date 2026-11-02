# Hardware and Software Inventory (Home Lab)

Inventory of the devices and software in my home practice environment. Serial numbers are masked to the last four characters, and hardware UUIDs are left out, because device identifiers should not be published.

## How the data was collected
- Hardware: `system_profiler SPHardwareDataType`
- Operating system: `sw_vers`
- Software versions: each tool's `--version` command
- Collected on 11/01/2026

## Hardware

| Asset ID | Device | Model | Chip | Memory | Serial (masked) | OS and version | Assigned user | Location | Status |
|---|---|---|---|---|---|---|---|---|---|
| HW-001 | Laptop | MacBook Neo (Mac17,5) | Apple A18 Pro, 6 cores (2 performance, 4 efficiency) | 8 GB | ****TF5W | macOS 26.5.2 (build 25F84) | Chaitanya | Home office | In use |

## Software

| Software | Version | Purpose | Installed on |
|---|---|---|---|
| Git | 2.50.1 (Apple Git-155) | Version control | HW-001 |
| Python | 3.15.2 | Scripting and data handling | HW-001 |
| Docker | 29.9.2 (build a82e528) | SQL Server lab container | HW-001 |
| Claude Code | 2.1.312 | AI-assisted development | HW-001 |

## What this exercise practiced
- Collecting inventory data from the system with commands instead of typing it by hand.
- Giving each asset an ID, owner, location and status so it can be tracked.
- Protecting sensitive identifiers: serials masked, hardware UUIDs left out of a published document.