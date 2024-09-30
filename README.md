# Network Map Simulation of OSPF Protocol with Cisco packet Tracer

The provided network map done with Cisco Packet Tracer demonstrate and simulate how OSPF protocol work in an enterprise network.

![PacketTracer_OSPF.gif](https://github.com/IT-Support-L2/OSPF/blob/master/PacketTracer_OSPF.gif)

# What is OSPF protocol?

Open Shortest Path First (OSPF) is an IP routing protocol that uses a mathematical algorithm to calculate the most efficient path to direct traffic on IP networks. OSPF is an open standard and designated by the Internet Engineering Task Force (IETF) as one of several Interior Gateway Protocols (IGPs) within the family of TCP/IP protocols.

Based on link-state or shortest path first (SPF) technology, OSPF distributes routing information between routers in a single autonomous system (AS). This capability differentiates OSPF from older TCP/IP routing protocols, which were designed for less complex networks than those used today.

Using Dijkstra's shortest path algorithm, OSPF calculates the shortest path for all routers in an area of the AS to efficiently use network bandwidth and ensure scalability. The AS may be divided into multiple interconnected networks, such as a wide area network (WAN). The topology is visible only to the routers in the same area.

As a dynamic routing protocol, OSPF not only routes IP packets based on the destination IP address (given in the packet header), but it also detects topological changes in the AS. After detecting changes, OSPF calculates new, loop-free routes after a short period (known as convergence time) in which routing traffic is kept to a minimum.
 
All the routers in the same area of the OSPF network maintain the same link-state database that describes the area topology. Each router receives link-state advertisement (LSA) messages containing information about neighboring routers and path costs from the other routers in that area. Using these LSAs, each router generates the link-state database and uses the SPF algorithm to calculate a shortest-path spanning tree.

OSPF was designed and developed by the IETF for TCP/IP environments, mainly large enterprise networks. OSPF version 2 is defined in RFC 2328 of the IETF Network Working Group. This protocol is broadly implemented in enterprise routers. IPv6 revisions to this standard are captured in OSPF version 3 and defined in IETF RFC 5340.

### Advantages of Open Shortest Path First

There are several benefits to OSPF. One benefit of the OSPF protocol is that all routers in the AS have complete information about the network topology, which allows them to calculate routes that satisfy specific quality of service (QoS) requirements. This feature is particularly advantageous for traffic engineering.

Another benefit is that the routes can be calculated (and recalculated) very quickly when the network topology changes. Another way of saying this is that OSPF results in a shorter convergence time after a network change. For this reason, OSPF is a suitable protocol for large and/or heterogeneous networks where changes happen frequently.

Thirdly, routing traffic can be managed by dividing the AS into multiple areas. Doing so ensures that area topologies are kept separate, which reduces the size of the link-state database of each area as well as traffic, minimizing delays.

Yet another advantage of OSPF is that it supports area routing, a mechanism by which the network topology information within one area of the AS is hidden from routers in other areas. In this way, OSPF provides routing protection and reduces routing traffic.

Finally, OSPF provides equal-cost multipath (ECMP) routing in which traffic with the same source and destination is transmitted across multiple paths of equal cost. ECMP routing helps with traffic load balancing and network bandwidth optimization.

### Drawbacks of Open Shortest Path First

OSPF has a couple of drawbacks. It was developed for large networks, for example, so it is not suitable for small networks. Also, the protocol is more complicated to configure compared to older protocols like RIP.
