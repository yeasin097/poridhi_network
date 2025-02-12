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