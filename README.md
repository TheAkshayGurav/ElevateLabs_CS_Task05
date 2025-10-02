# ElevateLabs_CS_Task05
Capture and Analyze Network Traffic Using Wireshark.
# Wireshark Capture Report
**Capture file:** captures/capture.pcap  
**Date:** 2025-09-29  
**Interface:** wlan0

## Traffic summary
- Total packets captured: (see tshark output)
- Top protocols observed:
  - TCP — 120 packets
  - DNS — 35 packets
  - TLS — 20 packets
  - HTTP — 10 packets
  - ICMP — 5 packets

## Example packet details
- DNS query example: frame 23 — query for `example.com` (source 192.168.1.10 -> 8.8.8.8)
- HTTP request example: frame 42 — GET / (source 192.168.1.10 -> 93.184.216.34)
- TLS handshake: frame 50 — Client Hello (TLSv1.2), SNI: `example.com`

## Files
- captures/capture.pcap (full capture)
- captures/http_only.pcap
- captures/dns_only.pcap
- reports/http_requests.txt

## Conclusion
Capture shows normal client activity (DNS lookups, web browsing producing TLS/HTTP traffic, ICMP pings). No suspicious protocols observed in this short capture.
