# 5 - Network layer

How would I be different after this?

* Understand network layers
* Know useful OFED network layer commands - locate HCA GID address







Network Layer: describes protocol for routing a packet **between subnets**

GRH

* present in a packet that traverses **multiple subnets**
* identifies the source and dest ports using GID (Layer 3 address placed in GRH) in the format of IPv6
* as packet traverses diff subnets, the **routers modify the GRH content and replace LRH**, but **source & dest GIDs do not change and protected by ICRC** field
* Routers recalculate VCRC but not ICRC



Network layer provides traffic routing between nodes that belong to diff subnets using GRH

* This includes unicast and multicast operations

Multicast traffic - one-to-many communication paradigm designed to improve the efficiency of communication between a set of end nodes







