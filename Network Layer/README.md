## What is Network Layer?

The Network Layer is the third layer of the OSI reference model and the second layer of the TCP/IP model, where it is referred to as the Internet Layer. The primary function of this layer is to assign source and destination IP addresses to packets. It encapsulates transport layer segments into packets by adding an IP header. Another key role of this layer is routing, which involves determining the best path for data to travel across networks.

## What is Routing?
Routing is the process of forwarding IP packets from one router to another to reach their destination. When a packet arrives at a router, the router examines its destination IP address, determines the best route, and forwards the packet accordingly.

There are two main types of routing algorithms: Static routing and Dynamic Routing.

### **Static Routing:**
Static routing is a type of routing where the network administrator manually configures the path for data packets. Unlike dynamic routing, static routes do not change automatically, even if a better path exists.

![](SVGs/NetworkTheoryStatic.drawio.svg)

In the given scenario, the server is sending packets to the client. The arrowed path represents the static route, which is not the best path. Since static routes are manually set, the router forwards packets along this predefined path, regardless of whether a more efficient route exists.

#### Why Is Static Routing Necessary?
1. **Control Over Routing (Security & Stability)**
* The arrowed path in the image, representing static routing, ensures that packets follow a predefined route, avoiding unnecessary deviations.
* This prevents unauthorized or unexpected traffic flow, which is useful in secure or restricted networks.

2. **No Routing Overhead (Faster Processing)**
* Static routes do not require CPU power or bandwidth for route calculations, unlike OSPF or BGP.
* The router simply follows the pre-configured path, making packet forwarding faster in stable networks.

3. **Useful in Small Networks**
* If a network has only a few routers, manually setting static routes is simple and efficient.
* In such cases, dynamic routing protocols add unnecessary complexity and consume extra bandwidth.

4. **Preferred Paths for Load Balancing**
* Even if the blue path is better, an administrator might want to distribute traffic to prevent congestion.
* Static routing allows manual traffic control, ensuring specific traffic flows through specific paths.
### **Dynamic Routing:** 
Routes that are automatically adjusted based on network conditions using routing protocols.