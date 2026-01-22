# Intro to InfiniBand

Objectives

* Describe Benefits
* List Most Common Usages
* Describe main features
* List major network components



#### InfiniBand Trade Association (IBTA)

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>



#### What is InfiniBand?

<figure><img src="../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>



#### Why InfiniBand?

<figure><img src="../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>



#### InfiniBand Key Features

<figure><img src="../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>



#### InfiniBand Bandwidth

<figure><img src="../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>



#### InfiniBand Port Structure

<figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>



#### InfiniBand Topologies

<figure><img src="../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>



#### InfiniBand Supported Topologies

<figure><img src="../../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>



#### Common InfiniBand Network Topology Icons

<figure><img src="../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>



#### InfiniBand Fabric Components

<figure><img src="../../.gitbook/assets/image (91).png" alt=""><figcaption></figcaption></figure>

Gateway / Bridge - A device that moves packets from an InfiniBand fabric to an Ethernet network and vice versa

Switch - A device that routes packets between different nodes with the local InfiniBand subnet

Host Channel Adapter - A device that terminates an InfiniBand link, executes transport-level functions and supports the verbs interface

Router - A device that transports packets between different InfiniBand subnets



#### Low-latency

<figure><img src="../../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure>



#### Simplified Management

<figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>



#### Network Scale-out

<figure><img src="../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

(**Theoretical:** The InfiniBand specification allows for up to 48,000 nodes per subnet due to its 16-bit Local Identifier (LID) system.)

<figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>





#### CPU Offloads

<figure><img src="../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

Traditional (No CPU offloads)

<figure><img src="../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>



CPU Offloads with RDMA Programming

<figure><img src="../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>



GPU Direct RDMA

<figure><img src="../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>





#### Fabric Resiliency - Self-healing Networking

Key required features include a stable network with minimum link failures and the fastest traffic recovery

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>



#### Load-balancing

<figure><img src="../../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>



#### Quality of Service

<figure><img src="../../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>



#### SHARP - Collective Operations Offload

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

