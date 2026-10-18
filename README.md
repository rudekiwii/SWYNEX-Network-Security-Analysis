# SWYNEX — Network Security Analysis

## Overview
This project documents a defensive network traffic analysis exercise completed as Task 2 of my SWYNEX internship.

## Objective
To analyze network traffic in a controlled Kali Linux virtual environment using Wireshark, identify observed protocols, and document findings supported by packet evidence.

## Tools Used
- Kali Linux
- Oracle VirtualBox
- Wireshark 4.6.6

## Analysis Performed
- Captured traffic from the `eth0` network interface.
- Examined DNS, TCP, and TLS traffic using display filters.
- Reviewed Protocol Hierarchy and TCP Conversations.
- Prepared a defensive network security analysis report.

## Key Observations
TCP traffic and TLS 1.3 application-data packets were observed during the capture. These observations alone do not establish malicious activity or a confirmed vulnerability.

See [`network-security-analysis-report.md`](network-security-analysis-report.md) for the methodology, observations, limitations, and recommendations.

## Evidence
Wireshark screenshots will be added to the [`evidence/`](evidence/) directory.

## Scope and Limitations
Analysis was limited to traffic visible to the Kali Linux VM during the capture period. Encrypted TLS application data was not interpreted as plaintext. Conclusions are limited to the available evidence.

## Disclaimer
This project was conducted for educational and defensive security analysis in a controlled lab environment.

