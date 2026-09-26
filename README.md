Wireshark Network Traffic Analysis

Practical network traffic analysis and PCAP investigation using Wireshark.

🎯 Project Objective

The objective of this project is to develop practical skills in network traffic analysis using Wireshark by examining packets, analyzing common network protocols, investigating PCAP files, and identifying network communication patterns.

Through hands-on practice, I learned how to inspect packet-level information, understand communication between hosts, use Wireshark filters and investigation features, and recognize network activity that may require further security investigation.

🛠️ Tools Used

- Wireshark
- Kali Linux
- PCAP files
- Web browser
- GitHub

📚 Things Covered

TCP

- 3-way handshake
- SYN, SYN/ACK and ACK
- FIN and RST
- Retransmissions
- Duplicate ACKs
- TCP window size
- TCP streams

DNS

- DNS query and response
- A records
- AAAA records
- CNAME records
- MX records
- Failed DNS queries
- Suspicious domains
- DNS tunneling basics

HTTP

- GET and POST requests
- HTTP status codes
- User-Agent
- Host header
- URLs
- File downloads

TLS/HTTPS

- TLS handshake
- Client Hello
- Server Hello
- SNI
- TLS versions
- Certificates
- Visible vs encrypted information
- ALPN

IP

- Source and destination IP
- Private and public IP addresses
- TTL
- IP fragmentation
- ICMP
- Traffic direction

Wireshark Features

- Display filters
- Follow TCP Stream
- Protocol Hierarchy
- Conversations
- Endpoints
- I/O Graphs
- TCP Stream Graphs

Security Investigation

- Port scanning
- Repeated SSH attempts
- Brute-force patterns
- Unusual DNS traffic
- HTTP scanning
- Large data transfers
- Beaconing / C2-like communication

🧪 Practical Analysis

1. TCP Analysis

Practiced identifying the TCP 3-way handshake:

SYN → SYN/ACK → ACK

Also analyzed TCP flags, retransmissions, duplicate ACKs, window size and TCP streams.

2. DNS Investigation

Analyzed DNS queries and responses and examined domain names and different DNS record types.

3. HTTP Analysis

Inspected HTTP requests and responses, including request methods, status codes, Host headers, User-Agent information and URLs.

4. TLS/HTTPS Analysis

Inspected TLS communication, including Client Hello, Server Hello, SNI, TLS versions, certificates and information that remains visible while application data is encrypted.

5. IP Investigation

Analyzed source and destination IP addresses, traffic direction, TTL, ICMP and IP fragmentation.

6. Follow TCP Stream ⭐

Used:

Right-click TCP packet → Follow → TCP Stream

This allows the conversation between two endpoints to be examined when the traffic is not encrypted.

7. Wireshark Statistics

Practiced using:

Statistics →

- Protocol Hierarchy
- Conversations
- Endpoints
- I/O Graphs
- TCP Stream Graphs

These features help provide an overview of traffic within a PCAP.

8. Suspicious Activity Investigation

Practiced looking for patterns that may require further investigation:

- Port scanning
- Repeated SSH attempts
- Brute-force patterns
- Unusual DNS traffic
- HTTP scanning
- Large data transfers
- Beaconing / C2-like communication

«A suspicious pattern does not automatically mean malicious activity. Additional investigation and context are required.»

🔎 Useful Wireshark Filters

TCP

tcp.flags.syn == 1
tcp.flags.reset == 1
tcp.analysis.retransmission
tcp.stream

DNS

dns
dns.qry.name
dns.flags.response == 0

HTTP

http
http.request
http.response.code
http.request.method == "POST"

TLS

tls
tls.handshake
tls.handshake.extensions_server_name

IP

ip.addr == 192.168.31.195
ip.src == 192.168.31.195
ip.dst == 192.168.31.195

📸 Practical Evidence

Screenshots from my Wireshark practical analysis are stored in the "screenshots/" directory.

TCP Analysis

"TCP Analysis" (screenshots/tcp-analysis.png)

DNS Analysis

"DNS Analysis" (screenshots/dns-analysis.png)

TLS/HTTPS Analysis

"TLS Analysis" (screenshots/tls-analysis.png)

Follow TCP Stream

"TCP Stream" (screenshots/tcp-stream.png)

Wireshark Statistics

"Statistics" (screenshots/statistics.png)

🛡️ SOC Relevance

Wireshark is useful for network-based security investigations. The skills practiced in this project can support tasks such as:

- Investigating network alerts
- Examining suspicious connections
- Analyzing IP addresses and ports
- Investigating DNS activity
- Reviewing PCAP files
- Understanding TCP communication
- Examining unencrypted network conversations
- Identifying traffic patterns that require further investigation

📌 Conclusion

This project provided hands-on experience with Wireshark and network traffic analysis. I practiced analyzing common protocols, investigating PCAP traffic, using display filters, and examining network communication at the packet level.

These practical exercises helped me build a foundation for SOC and network security investigations.
