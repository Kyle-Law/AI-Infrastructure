# Quiz

Virtual lanes are used by what mechanism?&#x20;

Question 1Select one:

Service Level

Virtualization

Quality of Service :white\_check\_mark:

CRC

Forwarding Table

#### Question 2

What are the two types of InfiniBand packets?&#x20;

Question 2 Select one or more:

Management :white\_check\_mark:

Frame

Local Routing Header

Data :white\_check\_mark:

#### Question 3

What is the purpose of the **Linear Forwarding Table**?

Question 3Select one:

Ensures incoming packets are sent out the correct port  :white\_check\_mark:

Load balances packet traffic&#x20;

Maps packets to a specific port

Forwards database table traffic through defined ports

Used to store ACKs

<details>

<summary>Explanation</summary>

the purpose of the Linear Forwarding Table (LFT) is to ensure incoming packets are sent out the correct port,.\
Explanation

* Mechanism: InfiniBand **switches** are the fundamental components for routing traffic **within** a subnet. When a switch receives a packet, it **examines the Destination Local Identifier (DLID) in the packet's Local Route Header (LRH)**,.
* Table Lookup: The switch uses this DLID as an **index** to look up an entry in its forwarding table. In the case of the Linear Forwarding Table, the table **contains a list of port numbers**.
* Egress Determination: Each entry in the LFT specifies the specific outbound port to which a packet with that corresponding LID should be forwarded.
* Configuration: **These tables are configured and loaded by the Subnet Manager (SM)** during fabric initialization and updated as the topology changes to ensure all endports remain reachable,,.<br>

While the Subnet Manager may use these tables to implement destination LID-based load sharing across multiple paths, the primary functional purpose of the LFT itself is to provide the port-to-LID mapping necessary to relay packets to their proper destination,.

other choices remain technically incorrect for the LFT:

* Load balancing: LFTs are static; they don't dynamically shift traffic to balance loads.
* Database table traffic: This is a play on the word "table" and is irrelevant to hardware switching.
* **Store ACKs: This is a function of the Host Channel Adapter (HCA) end-nodes**, not the switch forwarding table.

</details>









#### Question 4

What is a virtual lane?

Question 4Select one:

A Mechanism to create multiple virtual links within a single physical link :white\_check\_mark:

VMware network virtualization of physical adapters &#x20;

A network lane used by virtualization software

A physical link

A Lane that is used by virtual machines (VMs)

