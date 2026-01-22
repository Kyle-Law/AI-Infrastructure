# Quiz

Which of the following sentences regarding the subnet manager’s roles are true?\
(Select two)

Question 1

The subnet manager assigns Local Identifiers (LIDs) to nodes. :white\_check\_mark:

The subnet manager routes packets based on the destination LID.

The subnet manager uses Management datagrams (MADs) to configure the subnet. :white\_check\_mark:

The subnet manager assigns Global Unique Identifiers (GUIDs) to nodes.

Explanation

* **The subnet manager assigns Local Identifiers (LIDs) to nodes.** The subnet manager (SM) is responsible for discovering the network topology and assigning a unique Local Identifier (LID) to every port connected to the InfiniBand network. This LID is used for routing packets within the local subnet.
* **The subnet manager uses Management datagrams (MADs) to configure the subnet.** The SM communicates with other nodes and switches in the subnet using a specific type of message called Management Datagrams (MADs) to perform its configuration and management tasks.&#x20;

Why other options are incorrect

* **The subnet manager routes packets based on the destination LID.** The subnet manager _assigns_ the LIDs and _calculates and programs the switch forwarding tables_, but the actual _routing_ of packets based on the destination LID is performed by the **switches** and Host Channel Adapters (HCAs) within the fabric itself, not the SM.
* **The subnet manager assigns Global Unique Identifiers (GUIDs) to nodes.**&#x47;lobal Unique Identifiers (GUIDs) are generally **hard-coded** or assigned during the manufacturing process to the hardware (like the HCA or switch ports) and are globally unique; they are not assigned by the subnet manager. The SM uses these GUIDs during the discovery phase to identify devices.&#x20;



#### Question 2

**Question text**

Which of the following headers are NOT read by an InfiniBand layer 3 router?

Question 2 Select one:

Extended Transport Header (ETH) :white\_check\_mark:

Invariant CRC & Variant CRC (ICRC and VCRC)

Local Route Header (LRH)

Global Route Header (GRH)

<figure><img src="../../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

Note: basically  L3 can read L2 and L3

#### Question 3

**Question text**

Which of the following sentences regarding Global Unique Identifiers (GUIDs) and Local Identifiers (LIDs) is true?&#x20;

Question 3Select one:

GUIDs are carried in the layer 2 header called the LRH. &#x20;

GUIDs are carried in the layer 3 header called the GRH.

LIDs are carried in the layer 2 header called the LRH.   :white\_check\_mark:

LIDs are carried in the layer 3 header called the GRH.  &#x20;

#### Explanation

An InfiniBand layer 3 router is responsible for routing packets between different subnets, using the 128-bit Global Identifiers (GIDs) in the **Global Route Header (GRH)**. The LRH contains the Local Identifiers (LIDs), which are only significant within a single subnet and are used by switches for local forwarding. Therefore, the router, operating at Layer 3 (Network Layer) to route _between_ subnets, does not need to read the LRH for its core routing function, as the LRH is part of the Layer 2 (Link Layer) forwarding mechanism.&#x20;

#### Why other options are incorrect

* **Extended Transport Header (ETH)**: This header is part of the transport layer information and not relevant to the network layer routing decision. (Note: InfiniBand uses various transport headers like BTH, RETH, DETH, etc., and not a generic "ETH" acronym, but these are handled at the transport layer).
* **Invariant CRC & Variant CRC (ICRC and VCRC)**: These are integrity check fields. The ICRC (Invariant CRC) is checked and the VCRC (Variant CRC) is updated by switches/routers at the link layer as the packet is forwarded through the network, which is a Layer 2 function, but the question asks about the router's Layer 3 function. The router's primary routing decision is based on the GRH (Layer 3), not the CRC fields.
* **Global Route Header (GRH)**: This is the header that the Layer 3 router _must_ read to perform routing between different InfiniBand subnets.&#x20;



#### Question 4

**Question text**

Which layer adds the Local Route Header (LRH) to the packet?

Question 4Select one:

Transport layer

Upper layer

Link layer :white\_check\_mark:

Network layer

Note: same source as Q2
