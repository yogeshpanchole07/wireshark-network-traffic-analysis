wireshark-network-traffic-analysis
SOC Analyst Beginner Project | Network Traffic Analysis using Wireshark (DNS, HTTP, TCP, TLS)  
---

 Objective  
To capture and analyze real-time network traffic using Wireshark and identify DNS queries, HTTP requests, TCP communication, and TLS handshake.

---

 Tool Used  
- Wireshark  

---
Environment  
- Interface: Wi-Fi  
- Local IP: 192.168.1.2  
- Gateway: 192.168.1.1  

---

 Traffic Analysis  

 DNS Analysis  
Filter Used: 
dns  

Observed:  
- Source: 192.168.1.2 → Destination: 192.168.1.1  
- Domains captured:
  - c.pki.goog  
  - mobile.events.data.microsoft.com  
  - sharepoint.com  

---

 HTTP Analysis  
Filter Used:  
http  

Observed Request: 
GET /r/r4.crl HTTP/1.1  

Details:  
- Source IP: 192.168.1.2  
- Destination IP: 172.217.26.3  
- Response: HTTP/1.1 304 Not Modified  

Headers:  
- Host: c.pki.goog  
- User-Agent: Microsoft-CryptoAPI/10.0  

---

 TCP Analysis  
Filter Used: 
tcp  

Observed: 
- Communication: 192.168.1.2 → 13.107.137.11  
- Port: 443 (HTTPS)  
- Multiple ACK packets observed  
- TCP segments reassembled  

---

 TLS Handshake  
Observed:  
- TLS Version: 1.2  
- Handshake: Client Hello  
- SNI: 201514-ipv4mte.gr.global.aa-rt.sharepoint.com  

---

 Screenshots  

[DNS](screenshots/dns-analysis.png)  
[HTTP](screenshots/http-request.png)  
[TCP](screenshots/tcp-analysis.png)  


---

 Project Files  

- capture.pcap  
- screenshots/  
- README.md  

---

 Key Learnings  

- DNS query and response analysis  
- HTTP request inspection  
- TCP packet behavior understanding  
- TLS handshake basics  
- Practical Wireshark usage  

---

 Conclusion  

This project demonstrates real-world network traffic analysis using Wireshark.  
It shows how a client communicates with external servers through DNS, HTTP, TCP, and encrypted TLS protocols.

---

References  

- https://www.wireshark.org/docs/  
- Based on real captured traffic analysis  
