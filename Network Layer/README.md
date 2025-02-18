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
Dynamic routing is a type of routing where routers automatically learn and update paths using routing protocols. Unlike static routing, dynamic routes can change based on network conditions, ensuring the best possible path for data packets.

![](SVGs/NetworkTheoryDynamic.drawio.svg)

In a given scenario, if a server is sending packets to a client, the arrowed path represents the dynamically selected route. Unlike static routing, if a better path exists, the routing protocol updates the route automatically, ensuring optimal data delivery.


#### How the Optimal Path is Selected?
Dynamic routing protocols evaluate multiple paths and select the most efficient one based on various network metrics. The decision is influenced by factors such as:

1. **Shortest Path (Hop Count & Cost Metrics)**
Some protocols, like RIP (Routing Information Protocol), prioritize the route with the fewest router hops between source and destination.
OSPF (Open Shortest Path First) assigns link costs based on bandwidth, preferring the path with the lowest total cost.

2. **Low Latency (Delay & Response Time)**
EIGRP (Enhanced Interior Gateway Routing Protocol) considers network delay when calculating the best path.
BGP (Border Gateway Protocol) can prioritize routes with the lowest latency based on real-time monitoring.

3. **Higher Bandwidth (Maximizing Data Transfer Capacity)**
OSPF assigns lower cost to higher-bandwidth links, making them preferable for data transmission.
EIGRP also considers bandwidth when computing the composite metric for path selection.


#### Why Is Dynamic Routing Necessary?
1. **Automated Route Updates (Efficiency & Adaptability)**
The dynamically chosen path continuously adapts to network changes, selecting the most efficient route.
If a link fails or a better path appears, the routing protocol updates the route automatically without manual intervention.

2. **Scalability for Large Networks**
In large or frequently changing networks, manually configuring static routes is impractical.
Dynamic routing protocols, such as OSPF, EIGRP, and BGP, allow routers to exchange and update routing information efficiently.

3. **Fault Tolerance & Redundancy**
If a link in the arrowed path fails, the routing protocol quickly recalculates and selects an alternative path.
This ensures high availability and minimizes downtime in enterprise networks.

4. **Load Balancing & Traffic Optimization**
Dynamic routing allows multiple paths to be utilized simultaneously, balancing network load.
Some protocols, like EIGRP, use unequal-cost load balancing to distribute traffic efficiently.

5. **Minimal Administrative Overhead**
Unlike static routing, administrators do not need to manually configure each route.
The network automatically adapts to topology changes, reducing the burden on network engineers.