# NETWORKWALKS-TARUN-B084-WK2-PM1-PM5-CYBERSECURITY

Week 2 cybersecurity internship practicals covering domain footprinting and Zenmap scanning.

## Overview

This repository documents W2-PM1, W2-PM5, and the practical results captured during the Networkwalks cybersecurity internship.

## Lab Configuration

| Item | Value |
| --- | --- |
| Platform | Kali Linux in Oracle VirtualBox |
| Network mode | NAT |
| Interface | `eth0` |
| Kali IP address | `10.0.0.2/24` |
| Gateway | `10.0.0.1` |
| Nmap version | 7.99 |

## Completed Activities

### W2-PM1 – Footprinting with Multiple Kali Tools

Used WHOIS, DNSRecon, NSLookup, WhatWeb, WAFW00F, and cURL to examine publicly available domain registration, DNS, and web response information for `networkwalks.com`.

### W2-PM5 – Zenmap Based Network Scanning

- Recorded the Kali network configuration and neighbour entry.
- Ran Nmap host discovery against `10.0.0.2` only.
- Ran a Zenmap Quick Scan against `127.0.0.1`; all 100 scanned TCP ports were closed.
- Ran a Zenmap Quick Scan against `scanme.nmap.org` (`45.33.32.156`): `22/tcp` open (SSH), `25/tcp` filtered (SMTP), `80/tcp` open (HTTP), and 97 ports closed.
- Captured Zenmap’s topology view of saved scan results.

## Key Observations

- WHOIS reported GoDaddy as registrar and HostGator name servers; DNSSEC was reported as unsigned.
- DNSRecon and NSLookup both showed `192.232.216.135` for `networkwalks.com`.
- WhatWeb reported Apache, WordPress 7.1.4, jQuery 3.7.1, and Bootstrap 7.1.4.
- WAFW00F reported ModSecurity (SpiderLabs).
- The cURL response showed HTTP/2 `200` and Apache. Cookie values are intentionally omitted.

## Screenshots

Add the practical screenshots to:

- `W2-PM1-Domain-Footprinting/screenshots/`
- `W2-PM5-Zenmap-Network-Scanning/screenshots/`

Do not upload the original cURL screenshot unless its cookie value has been redacted.

## Scope Note

The host-discovery command checked only `10.0.0.2`; no subnet-wide or multi-host scan is claimed. The topology screenshot shows results from separate saved scans, not hosts discovered together on one network. The `scanme.nmap.org` scan is documented separately from the `networkwalks.com` footprinting work.

These results are observations from the captured practicals and do not establish that vulnerabilities were present or absent.
