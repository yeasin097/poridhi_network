# OSI MODEL
## Introduction
The internet is a complex system. To manage complexity, we use the divide and conquer approach, breaking a large problem into smaller, manageable parts. Similarly, network communication is divided into seven layers, forming the OSI (Open Systems Interconnection) model. Each layer has a specific task and follows certain protocols or standards to ensure smooth communication.
## Why do we need the OSI model?
Think about building a house. Before construction starts, you need a blueprint—a clear plan that shows how everything will come together. Then, different teams work on different parts: one team lays the foundation, another builds the walls, electricians install wiring, and plumbers set up the water system. Each team follows a step-by-step process to make sure everything fits together properly.

Networking works the same way. The OSI (Open Systems Interconnection) model is like a blueprint for how devices communicate. It breaks the process into seven layers, where each layer has a specific job. This makes it easier to design, fix, and improve networks.

Without this structured approach, networking would be messy—just like a house built without a proper plan. Different devices might not work together, fixing issues would be harder, and upgrading systems would be a challenge. The OSI model helps ensure that all parts of a network communicate smoothly and efficiently.

![](./SVGs/OSIL1.drawio.svg)

## What is a protocol?
In networking, a protocol is a set of rules that defines how data is formatted, transmitted, and processed. It acts as a common language that allows computers and devices to communicate with each other.

For successful communication, both the sender and receiver must follow the same protocol. These protocols can be implemented in software, hardware, or both to ensure smooth data exchange.

Without network protocols, devices wouldn’t understand each other, making communication impossible. Some common network protocols include HTTP, TCP/IP, DNS, and FTP, each serving a specific purpose in data transmission.

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f9e43fa-84d5-4875-817c-c2e1af75d16e_1280x1664.gif)

## Layers of the OSI model.

## 7. Application Layer:
The Application Layer is the topmost layer of the OSI model. It is directly used by end-users and provides network services to applications like web browsers, email clients, and file-sharing software. This layer does not handle the actual data transmission but ensures that applications can communicate properly over a network. It is responsible for data creation, processing, and final delivery to the user.
![](./SVGs/OSIL7.drawio.svg)
For example, when a client requests a webpage, the HTTP protocol (which operates at the Application Layer) sends the request to the web server. The server processes the request, retrieves the webpage, and sends it back to the client's Application Layer, where the browser interprets and displays the content. Similarly, in an email exchange, SMTP (Simple Mail Transfer Protocol) ensures that emails are sent from the sender’s application to the recipient’s application layer via the network.

Key Protocols and Services:

* HTTP/HTTPS: For web browsing
* FTP: For file transfers
* SMTP/POP3/IMAP: For email
* DNS: For domain name resolution
* SSH: For secure remote access
* SNMP: For network management
* Telnet: For remote terminal access

#### Functions of Application Layer 
* Application Flow Control: This layer manages the dialogue between applications, determining when a program can send or receive data. For instance, in video streaming, it controls buffering and playback to ensure smooth content delivery despite network variations.
* Error Handling and Recovery: While lower layers handle network-related errors, the Application Layer manages application-specific errors. If a web page fails to load, it might show a 404 error page. For file transfers, it might implement checksums to verify data integrity or handle incomplete transfers.
* Service Advertisement and Discovery: Applications need to locate and identify available network services. DNS is a prime example - when you type "www.example.com", the Application Layer uses DNS to discover the corresponding IP address. Similarly, DHCP helps devices discover network configuration settings.

## 6. Presentation Layer:
The Presentation Layer is responsible for data formatting, encryption, and compression. It ensures that data sent from one system's application layer can be read by the application layer of another system. This layer acts as a translator between different data formats and encodings, making sure that data remains usable across different systems.
![](./SVGs/OSIL6.drawio.svg)
For example, when you download an image file, the Presentation Layer handles the conversion between different image formats (like JPEG to PNG) if needed. When streaming a video, it manages the compression to optimize data transmission while maintaining quality. For secure banking transactions, this layer handles the encryption of sensitive data before transmission and decryption upon receipt.

#### Functions of Presentation Layer
* Data Translation and Formatting: This layer converts data between different formats to ensure compatibility. For example, converting text between ASCII and EBCDIC, or handling different image formats (JPEG, PNG, GIF) across systems.
* Data Encryption/Decryption: Handles security by encrypting data before transmission and decrypting it upon receipt. This is crucial for secure communications like HTTPS websites, secure email, and online banking.
* Data Compression: Reduces the size of data for more efficient transmission while maintaining data integrity. When you send a large file attachment in an email, the Presentation Layer might compress it to reduce transmission time.
* Protocol Conversion: Manages the conversion between different protocols when necessary, ensuring that systems using different protocols can still communicate effectively.

## 5. Session Layer:
The Session Layer is responsible for establishing, maintaining, and terminating communications between applications. It manages the dialogue control between devices, ensuring that data exchange is organized and synchronized. This layer handles session establishment, maintenance, and termination, as well as authentication and security.

![](./SVGs/OSIL5.drawio.svg)

For example, when you start a video call, the Session Layer establishes the initial connection between your device and the recipient's device. It maintains this session throughout the call, handling any interruptions or disconnections. If your internet connection drops briefly, the Session Layer can often restore the session without requiring you to restart the entire call. Similarly, during a file transfer, if the connection is interrupted, the Session Layer can implement checkpointing to resume the transfer from where it left off rather than starting over.

#### Functions of Session Layer

* Session Establishment and Termination: This layer creates, manages, and ends sessions between applications. For instance, when you log into a remote server, the Session Layer establishes the connection, maintains it during your work, and properly closes it when you log out.
* Synchronization and Recovery: The Session Layer places checkpoints (synchronization points) in the data stream, allowing for recovery in case of failure. If a file transfer is interrupted at 75% completion, it can resume from that checkpoint rather than starting over.
* Dialog Control: Manages the communication flow between systems, determining which side can transmit at any given time (half-duplex or full-duplex). This is crucial in applications like online gaming where coordinated data exchange is essential.
* Connection Monitoring: Continuously tracks the status of the connection and can notify applications if a session is interrupted or terminated unexpectedly. This allows applications to take appropriate action, such as saving work or attempting to reconnect.

## 4. Transport Layer:
The Transport Layer is responsible for directing data to the correct applications using port numbers. When data arrives from the internet, this layer ensures it reaches the right application - email data goes to email clients, web data goes to browsers, and chat messages go to messaging apps. It's like a postal sorting system that makes sure each package reaches its correct destination within a building.
![](./SVGs/OSIL4.drawio.svg)
For example, when you're simultaneously browsing a website, checking email, and using a messaging app, the Transport Layer ensures each piece of data reaches the correct application by checking port numbers. Web traffic goes to port 80 (HTTP) or 443 (HTTPS), email might use port 25 (SMTP) for sending or port 110 (POP3) for receiving, and each messaging app has its designated port.

### Functions of Transport Layer

* Port Management: The primary function is managing communication between different applications through port numbers:
Web Browsers: Use ports 80 (HTTP) and 443 (HTTPS)
Email Clients: Use ports 25 (SMTP), 110 (POP3), 143 (IMAP)
File Transfer: Uses ports 20/21 (FTP)
Gaming Applications: Use various designated ports
DNS Services: Use port 53
Database Services: Often use port 3306 (MySQL) or 5432 (PostgreSQL)
* Connection Types:
TCP: Used when reliable delivery is crucial (file downloads, emails)
UDP: Used when speed is more important than reliability (video streaming, online gaming)

## 3. Network Layer: 
This is the most important layer of the OSI reference model. This layer append the source and destination IP address into the segment. Also this layer is responsible for routing. Routing is needed to deliver the intended packet into right destination.
#### Functions of Network Layer
* Fragmentation: Data is created on the upper layer big which can not sent over the network. This layer divides the data into smaller fragments based on the capacity of the channel.
* IP Addressing: If the data is intended to sent to a device which is in local network, the IP address is not necessary. But if the data is to sent a device which is not in the local network then the IP address is appended as packed header which consist source and destination IP address.
* Routing: Different routing protocols is used in this layer like BGP, RIP, OSPF. We will discuss it later.

![](./SVGs/OSIL3.drawio.svg)

## 2.Data Link Layer: 
When data travels through different physical mediums (like copper wire, fiber optic, or wireless), errors can occur during transmission. The Data Link Layer solves this problem by adding mechanisms to detect and retransmit damaged or lost frames. It acts like a quality control system, checking data packets for errors and requesting retransmission if needed.
![](./SVGs/OSIL2.drawio.svg)
For example, when you're downloading a file over Wi-Fi, interference might corrupt some data packets. The Data Link Layer detects these corrupted frames using error detection methods (like [CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check) - Cyclic Redundancy Check), and requests retransmission of any damaged frames. It also handles duplicate frames that might occur during retransmission, ensuring data integrity.

#### Functions of Data Link Layer
* Framing: Data link layer divides the stream of bits coming from Physical layer into frames. Frames can be different size based on the protocol used. For example, maximum frame is for Ethernet (IEEE 802.3) is 1518 bytes and minimum 64 bytes including CRC.
* Physical Addressing: In the Local Area Network (LAN) data is not transmitted based on their IP address instead it transmission happens based on the 48 bits MAC address. When a device sends data over a network, the Data Link Layer encapsulates the data into frames and attaches the source MAC address (sender) and destination MAC address (receiver). Unlike private IP address, MAC address is unique for every device on the internet. 

![](https://media.fs.com/images/ckfinder/ftp_images/tutorial/mac-addresse-numbers.jpg)


## 1. Physical Layer:
The Physical Layer is the foundation of the OSI model, responsible for transmitting raw bits (0s and 1s) over physical media. It converts digital data into signals that can travel through different types of physical connections like copper cables, fiber optic cables, or wireless signals through the air. Think of it as the actual "highway" where data travels.
![](./SVGs/OSIL1.drawio.svg)
For example, when you send a text message, the Physical Layer converts the digital data into electrical signals in your phone, transmits them as radio waves through the air to a cell tower, then possibly through fiber optic cables as light pulses, before being converted back to electrical signals at the recipient's device.
#### Functions of Physical Layer
* Encoding and Signaling: Converts digital data (0s and 1s) into signals appropriate for transmission, such as electrical signals (wired networks) or radio waves (Wi-Fi).

![](https://miro.medium.com/v2/resize:fit:4800/format:webp/1*Fu9IQ-mFYsTKF9pL0kQACw.png)
![](https://www.qrg.northwestern.edu/projects/vss/docs/media/Communications/FM.gif)
* Data Transmission and Reception: Ensures that data is properly sent and received over the communication channel. Different transmission media include wired networks (Ethernet) and wireless networks (Wi-Fi, Bluetooth).







