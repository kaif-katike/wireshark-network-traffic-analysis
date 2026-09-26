🔍 Practical Skills & Investigations

1. TCP Analysis

Learned to identify:

- 3-way handshake: "SYN → SYN/ACK → ACK"
- FIN and RST packets
- TCP retransmissions
- Duplicate ACKs
- TCP window size
- TCP streams

Useful filters:

tcp.flags.syn == 1
tcp.flags.reset == 1
tcp.analysis.retransmission
tcp.stream

2. DNS Investigation

Practiced understanding:

- DNS queries and responses
- A, AAAA, CNAME and MX records
- Failed DNS queries
- Domain names in DNS traffic
- Basics of suspicious DNS behavior

Useful filters:

dns
dns.qry.name
dns.flags.response == 0

3. HTTP Analysis

Practiced inspecting:

- GET and POST requests
- HTTP status codes
- User-Agent
- Host header
- URLs
- HTTP file transfers

Useful filters:

http
http.request
http.response.code
http.request.method == "POST"

4. TLS/HTTPS Analysis

Practiced inspecting:

- TLS handshake
- Client Hello
- Server Hello
- SNI
- TLS versions
- Certificates
- Visible vs encrypted information

Useful filters:

tls
tls.handshake
tls.handshake.extensions_server_name

5. IP Investigation

Practiced identifying:

- Source vs destination IP
- Private vs public IP addresses
- TTL
- IP fragmentation
- ICMP traffic
- Traffic direction

Example filters:

ip.addr == 192.168.31.195
ip.src == 192.168.31.195
ip.dst == 192.168.31.195

6. Follow TCP Stream ⭐

Practiced using:

Right-click packet → Follow → TCP Stream

This can reconstruct the conversation between two endpoints when the traffic is not encrypted.

7. Wireshark Statistics

Practiced using:

Statistics →

- Protocol Hierarchy
- Conversations
- Endpoints
- I/O Graphs
- TCP Stream Graphs

These features help provide a quick overview of network activity in a PCAP.

8. Suspicious Activity Investigation

Practiced looking for patterns associated with:

- Port scanning
- Repeated SSH connection attempts
- Brute-force patterns
- Unusual DNS traffic
- HTTP scanning
- Large data transfers
- Beaconing / C2-like communication

«Note: A suspicious pattern is not automatically malicious. Further investigation and context are required before determining what happened.»
