# TCP/IP MODEL
## Introduction
The OSI reference model consists of seven layers that represent a functional division of tasks required to implement a network. It serves as a conceptual tool to illustrate how various protocols and technologies work together to establish communication. However, it is not the only networking model that organizes tasks into layers and components. However, it's not the
only networking model that attempts to divide tasks into layers and components. A more practical and widely used model is the TCP/IP (Transmission Control Protocol/Internet Protocol) model. 

The TCP/IP  model is the foundation of modern networking and the internet. It defines how data is transmitted and received across networks, ensuring seamless communication between devices worldwide.

## TCP/IP VS OSI
Both the TCP/IP model and the OSI model are used to describe how data is transmitted over a network. While the OSI model is a theoretical framework, the TCP/IP model is a practical and widely used protocol suite.

![](./SVGs/TCPIP-OSI.drawio.svg)

* In TCP/IP's Application Layer, the functions of three OSI layers (Application, Presentation, Session) are merged into a single layer. This means all application services, data formatting, and session control happen in one unified layer instead of three separate ones.

* The Transport Layer stays identical in both models - performing the same end-to-end communication functions. No merging was needed here as both models handle transport tasks similarly.

* The Network Layer of OSI becomes the Internet Layer in TCP/IP. This was mainly a name change to reflect its role in internet communications, while keeping similar routing and addressing functions.

* TCP/IP's Network Access Layer combines the functions of OSI's bottom two layers (Physical and Data Link). Instead of separating physical transmission from basic data handling, TCP/IP handles both hardware-level tasks in one layer.

## Layers of TCP/IP

## 4. Application Layer:
The Application Layer in the TCP/IP model is responsible for interacting with end-user applications and providing network services. Since the TCP/IP model does not have separate Presentation and Session layers like the OSI model, the Application Layer performs the functions of all three layers of OSI model.
* **Application layer functions:** Provides network services directly to applications (e.g., web browsing, email, file transfer). Examples of protocols: HTTP, HTTPS, FTP, SMTP, DNS, Telnet.
* **Presentation layer functions:** Handles data formatting, encryption, and compression. Converts data into a format that applications can understand (e.g., JPEG, MP3, MP4, TLS encryption).
* **Session Layer functions:** Manages and maintains communication sessions. Responsible for establishing, maintaining, and terminating sessions between devices (e.g., NetBIOS, RPC, SOCKS).

## 3. Transport Layer:
The Transport Layer in the TCP/IP model is responsible for end-to-end communication, ensuring reliable or fast data transfer between devices. It provides mechanisms for error detection, flow control, and connection management.
* **Connection-Oriented Communication:** Ensures reliable data transmission using acknowledgments and retransmissions (e.g., TCP).
* **Connectionless Communication:** Provides fast, lightweight communication without establishing a connection (e.g., UDP).
* **Error Detection and Correction:** Ensures data integrity using checksums and retransmissions.
* Flow Control: Regulates data transmission to prevent congestion or packet loss (e.g., TCP windowing).
* **Multiplexing and Demultiplexing:** Uses port numbers to distinguish multiple applications running on a device (e.g., port 80 for HTTP, port 443 for HTTPS).

## 2. Internet Layer:
The Internet Layer in the TCP/IP model is responsible for addressing, routing, and delivering packets across networks. It enables communication between devices on different networks by providing logical addressing and path determination.

* **Logical Addressing:** Uses IP addresses to uniquely identify devices on a network.
* **Packet Forwarding and Routing:** Determines the best path for data to travel across networks (e.g., using routing protocols like OSPF, BGP).
* **Fragmentation and Reassembly:** Splits large packets into smaller fragments for transmission and reassembles them at the destination.
* **Error Handling and Diagnostics:** Uses protocols like ICMP for error reporting and network diagnostics (e.g., Ping, Traceroute).

## 1. Network Access Layer (Link Layer):
The Network Access Layer (also called the Link Layer) is responsible for physical transmission of data and managing access to the network medium. It ensures that data is correctly formatted and transmitted over the physical network.
* **Physical Addressing:** Uses MAC addresses to identify devices within a local network.
* **Framing:** Encapsulates data into frames for transmission over the network medium.
* **Error Detection and Correction:** Uses techniques like CRC checks to detect errors in transmitted frames.
* **Media Access Control:** Determines how devices share and access the network medium (e.g., CSMA/CD in Ethernet).
* **Physical Transmission:** Defines how data is physically transmitted over cables, wireless signals, or fiber optics.

## TCP/IP Layers and Their Protocols
![](./SVGs/TCPIP-Protocols.drawio.svg)

### Application Layers Protocols:
* **DNS (Domain Name System):**  Translates human-readable domain names (e.g., google.com) into IP addresses (e.g., 142.250.190.78), allowing computers to locate servers.
* **DHCP (Dynamic Host Configuration Protocol):** Automatically assigns IP addresses and network configurations (subnet mask, gateway, DNS servers) to devices on a network.
* **SMTP (Simple Mail Transfer Protocol):** Used for sending emails between mail servers and from email clients to servers. It works with POP3 or IMAP for receiving emails. Example: When you send an email via Gmail (you@gmail.com to friend@yahoo.com), Gmail’s SMTP server (smtp.gmail.com) forwards it to Yahoo’s mail server.
*  **FTP (File Transfer Protocol):** Transfers files between a client and a server over a network, supporting both upload and download operations.
* **HTTP (Hypertext Transfer Protocol):** Enables web communication by transferring web pages, images, and other resources between a client (browser) and a web server.


