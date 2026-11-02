# IT Support Operations Lab

## Overview

This lab is a hands-on learning project for practical IT support, troubleshooting and systems administration skills. Each exercise is performed, documented and committed with Git, so the record shows what was done and when.

The exercises use macOS and other tools available in a personal environment. Windows and Active Directory exercises will be added only after they have actually been performed.

## Learning Objectives

- Develop systematic troubleshooting skills.
- Understand network connectivity and DNS operations.
- Inspect network interfaces, routing and network configuration.
- Practice help desk ticket documentation and escalation.
- Practice IT asset inventory and documentation.
- Write user-facing knowledge base articles in plain language.
- Build familiarity with Windows desktop support and Active Directory (planned).
- Maintain technical records using Git and Markdown.

## Project Structure

```text
5_it_support_operations/
├── README.md
├── 02_network_troubleshooting/
│   ├── 01_basic_connectivity_test.md
│   ├── 02_dns_lookup_test.md
│   ├── 03_traceroute_test.md
│   └── 04_network_configuration_inspection.md
├── 03_help_desk_tickets/
│   └── ticket_log.md
├── 04_asset_inventory/
│   └── hardware_software_inventory.md
├── 05_knowledge_base/
│   ├── kb01_user_cannot_sign_in.md
│   └── kb02_printer_offline.md
├── 06_windows_support/                    (planned)
│   └── README.md
└── 07_user_access_and_active_directory/   (planned)
    └── README.md
```

## Completed Exercises

| # | Exercise | Status | What it shows |
|---|---|---|---|
| 01 | [Basic connectivity test](02_network_troubleshooting/01_basic_connectivity_test.md) | Completed | `ping`, packet loss and response times; 0% loss |
| 02 | [DNS lookup](02_network_troubleshooting/02_dns_lookup_test.md) | Completed | `nslookup`, configured DNS server, returned IPv4 addresses |
| 03 | [Traceroute](02_network_troubleshooting/03_traceroute_test.md) | Completed | `traceroute`, network path, destination reached in six hops |
| 04 | [Network configuration inspection](02_network_troubleshooting/04_network_configuration_inspection.md) | Completed | `ifconfig`, default gateway with `route`, `scutil` DNS and VPN settings, `dig`; tunnel interfaces identified without assuming an active VPN |
| 05 | [Help desk ticket log](03_help_desk_tickets/ticket_log.md) | Simulated | Eight tickets classified by category and priority; 6 of 8 resolved at first contact, 2 escalated with scope |
| 06 | [Hardware and software inventory](04_asset_inventory/hardware_software_inventory.md) | Completed | Data collected with system commands; asset IDs, versions; serials masked |
| 07 | [KB01: I can't sign in](05_knowledge_base/kb01_user_cannot_sign_in.md) | Completed | User-facing steps in plain language, with what to send the help desk |
| 08 | [KB02: Printer shows offline](05_knowledge_base/kb02_printer_offline.md) | Completed | User-facing steps, with a rule for when to escalate |

## Planned Learning Areas

**User access scenarios**
- User account concepts, authentication and authorization.
- Access permissions and Active Directory fundamentals.

**Windows support**
- Windows troubleshooting and command-line diagnostics.
- Application and workstation support scenarios.

## Documentation Standards

Each completed exercise includes:

- Objective
- Environment
- Commands or procedures performed
- Findings and observations
- Troubleshooting conclusion
- Scope and limitations
- Completion status

## Tools and Technologies

- macOS Terminal
- Git and GitHub
- Markdown
- Network diagnostic utilities: `ping`, `nslookup`, `traceroute`, `dig`
- macOS network configuration utilities: `ifconfig`, `route`, `scutil`
- System inventory: `system_profiler`, `sw_vers`

## Environment and Limitations

This is a personal learning and demonstration environment.

- Exercises are performed on personal systems or simulated scenarios.
- No production corporate network or live enterprise help desk is used.
- Fictional users and devices are used for simulated support tickets.
- Device identifiers are masked or left out of published documents.
- Windows administration and Active Directory experience will be documented only after the exercises have actually been performed.
- No production systems or user accounts are modified.

## Progress Tracking

- **Planned:** not started.
- **In Progress:** currently being practiced.
- **Completed:** performed and documented.
- **Simulated:** practiced with a fictional scenario or test environment.

## Purpose

This project demonstrates continuous hands-on learning in IT support operations, troubleshooting, technical documentation and systems administration fundamentals, with an accurate record of what has and has not been done.