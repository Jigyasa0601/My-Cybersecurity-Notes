# Room: INTRODUCTORY NETWORKING <br>
**TryHackMe link**: [INTRODUCTORY NETWORKING ROOM](https://tryhackme.com/room/introtonetworking?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a5ba5be99ab54f7c1dacca7) <br>
**Category**: Networking<br>
# What I Learned <br>
1.The OSI Model()<br>
2.The TCP/IP Model<br>
3.How these models look in practice<br>
4.An introduction to basic networking <br>
# The OSI Model(Open Systems Interconnection)<br>
The OSI model is a seven-layer framework that explains how data moves across a network. It breaks down complex communication into smaller,managable steps.<br>
The OSI model consists of seven layers:<br>
1.Application<br>
2.Presentation<br>
3.Session<br>
4.Transport<br>
5.Network<br>
6.Data Link<br>
7.Physical<br>
**Trick to remember**: All People Seem To Need Data Processing.<br>
# The TCP/IP Model<br>
The TCP/IP model is, in many ways, very similar to the OSI model. It's a few years older, and serves as the basis for real-world networking. The TCP/IP model consists of four layers: Application, Transport, Internet and Network Interface. Between them, these cover the same range of functions as the seven layers of the OSI Model.<br>
The layesrs of the TCP/IP model: <br>
1.Application<br>
2.Transport<br>
3.Internet<br>
4.Network Interface<br>
# Comparison between the TCP/IP and OSI models.<br>
![View the image to see the comparison if these two models.](My-Cybersecurity-Notes/networking/images/image.png)<br>
# ENCAPSULATION AND DE-ENCAPSULATION<br>
Encapsulation is the process of adding headers to a message at each layer of transmission from application to physical. Decapsulation is the reverse process of removing the headers at each layer of receipt. Headers contain addressing information like port numbers, IP addresses, and MAC addresses to direct the message properly through networks and to the destination host. Encapsulation and decapsulation are necessary to send and receive messages across different network layers and systems.<br>
**Encapsulation**<br>
What it does: Prepares data for transmission.<br>
How it works: Each layer adds its own addressing and control info (header) to the data from the layer above.<br>
Example: Data -> Segment (Transport) -> Packet (Network) -> Frame (Data Link) -> Bits (Physical).<br>
**Decapsulation**<br>
What it does: Prepares data for use by the application.<br>
How it works: Each layer reads its specific header, strips it off, and passes the remaining payload up to the next layer.<br>
Example: Bits -> Frame -> Packet -> Segment -> Original Data.<br>
![These chart shows how at each layer data transmission works.](My-Cybersecurity-Notes/networking/images/image-1.png)<br>
# NETWORKING TOOLS <br>
Networking tools split into physical hardware used for cable installation and digital software used for network management, monitoring, and troubleshooting.<br>
Digital Software Tools:<br>
1.Wireshark: Captures and analyzes network packet traffic for security and troubleshooting.<br>
2.Nmap: Scans networks to find live hosts, open ports, and operating systems.<br>
3.Ping / Traceroute: Tests connection speed, latency, and the exact path data takes.<br>
4.PuTTY: Acts as an SSH/Telnet client to remotely configure routers and switches.<br>
5.SolarWinds / PRTG: Monitors overall network health, bandwidth usage, and device uptime.<br>