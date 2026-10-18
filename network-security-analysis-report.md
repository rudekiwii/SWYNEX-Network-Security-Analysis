# Network Security Analysis Report

## 1. Project Overview

**Internship:** SWYNEX  
**Task:** Task 2 — Network Security Analysis  
**Tool:** Wireshark 4.6.6  
**Environment:** Kali Linux running in Oracle VirtualBox

## 2. Objective

To capture and analyze network traffic in a controlled lab environment, identify the protocols observed, and document potential security concerns based on available packet evidence.

## 3. Scope

The analysis was performed on network traffic visible to the Kali Linux virtual machine through its `eth0` interface. The activity was limited to defensive packet analysis of traffic available in the lab environment.

## 4. Tools and Methodology

- Wireshark 4.6.6 for packet capture and inspection.
- Display filters to examine DNS, TCP, and TLS traffic.
- Protocol Hierarchy to review protocols present in the capture.
- TCP Conversations to inspect communication between endpoints.

## 5. Observations

### 5.1 TCP Traffic

TCP packets were observed between `10.0.2.15` and `101.2.55.20`. Packets included acknowledgements and data segments involving port 443.

### 5.2 TLS Traffic

TLS 1.3 application-data packets were visible in the capture. This indicates encrypted application traffic was present. The contents of encrypted application data were not interpreted as plaintext.

### 5.3 DNS Traffic

The DNS display filter was applied to examine DNS packets. Specific DNS queries and responses should be documented from the saved capture where present.

### 5.4 Protocol Statistics

Wireshark's Protocol Hierarchy and TCP Conversations views were used to examine protocol distribution and observed TCP communications. Exact counts and additional findings should be recorded from the saved results.

## 6. Security Assessment

The observed TCP and TLS traffic is not, by itself, evidence of malicious activity. No confirmed attack or vulnerability is claimed in this report based solely on the observations described above.

A more complete assessment would require reviewing the relevant packet details, DNS responses, connection patterns, and any unusual or unexpected behavior in the capture.

## 7. Recommendations

- Use encrypted protocols such as HTTPS wherever appropriate.
- Keep systems, browsers, and network software updated.
- Investigate unexpected destinations, repeated connection failures, and unusual traffic patterns when supported by packet evidence.
- Retain packet captures securely and avoid sharing sensitive network data publicly.
- Document timestamps, packet numbers, and supporting evidence for any suspected security incident.

## 8. Limitations

This assessment covers only the traffic visible to the Kali Linux VM during the capture period. Encrypted TLS application data could not be interpreted as plaintext. The observations do not establish the security status of the entire network.

## 9. Conclusion

Wireshark was used to capture and inspect network traffic in a controlled virtual lab environment. TCP and TLS traffic were observed, and display filters and protocol statistics were used as part of the analysis workflow. Further investigation of specific packet evidence would be needed before identifying any confirmed security incident.

## 10. Evidence

The following evidence should accompany this report:

- Wireshark interface and version.
- Live packet capture.
- DNS, TCP, and TLS display-filter results.
- Protocol Hierarchy results.
- TCP Conversations results.

Screenshots should be stored in the repository's `evidence/` directory.
