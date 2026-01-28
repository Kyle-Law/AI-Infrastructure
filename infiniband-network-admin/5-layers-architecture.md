# 5 Layers Architecture

5 layers architecture

1. what are the 5 layers architecture for Infiniband?

Physical

* specifies how bits are placed on the wire to form symbols -> used for framing, data symbols, and fill between packets
* specifies the signalling protocol

Link

* describes packet format and protocols
* 2 types of packets - Link mgt, data

1. Link management packet

* to train and maintain link operation
* created and consumed within Link Layer
* to negotiate operational params between ports at each end of the link
* to convey flow control credits and maintain link integrity
* never forwarded to other links

2. Data Packet

* convey IBA operations
* consist optional headers

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

#### LRH

* always present
* identifies local source and destination ports
* specifies SL and VL on which the packet travels
* VL changes as the packet traverses the subnet



SM

* assigns unique LIDs to each port of a channel adapter



2 CRCs in each packet

* Invariant CRC: static fields
* Variant CRC: all fields of the packet

> CRC stands for Cyclic Redundancy Check, a mechanism used primarily at the **Link Layer** for **error detection** to **ensure data integrity** as packets move across the fabric



Link Level flow control

* credit based method where the receiver on each link sends credits to the transmitter on the other end of the link
* per VL
* indicate the number of data packets that the receiver can accept on that VL
* Transmitter does not send data packets unless receiver indicates it has room
* VL15 = mgt VL not subject to flow control



### Network Layer

> describes protocol for routing a packet between subnets

#### GRH

* present in packet that traverses multiple subnets
* GID in IPv6 address format



Network

Transport

Upper Layer Protocols
