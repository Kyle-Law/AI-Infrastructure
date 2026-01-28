# Quiz

What are the maximum number of nodes allowed in an InfiniBand subnet?

Question 1Select one:

10,000

No limit

400

48,000 :white\_check\_mark:

500

<details>

<summary>Explanation</summary>



A single InfiniBand (IB) subnet can theoretically support up to 48,000 to 65,000 nodes, depending on the generation (e.g., SDR/DDR vs. HDR/NDR) and the capabilities of the Subnet Manager (SM). Practical limits are often determined by the 16-bit Local Identifiers (LIDs) used for addressing, with newer, more optimized SMs supporting higher node counts. Key details regarding InfiniBand subnet node limits:

* **Theoretical Limit:** The base specification, driven by 16-bit LIDs, allows for a large number of end-nodes, often cited around 48,000.
* **Practical Scaling:** Modern InfiniBand generations (EDR/HDR/NDR) can support up to 65,000+ nodes in a single subnet with optimized SM software.
* **Subnetting and Routing:** To scale beyond a single subnet, InfiniBand routers are used to connect multiple subnets, allowing for significantly larger networks.
* **Subnet Manager (SM):** An SM must manage the fabric, and larger, complex topologies may require robust SM implementations to handle node discovery and routing, notes [this ManKier page](https://www.mankier.com/8/opensm).&#x20;

</details>

#### Question 2

**Question text**

What command would you run to locate the GID of an HCA port?

Question 2Select one:

Ibaddr :white\_check\_mark:

ibv\_devices

ib\_get GID

ib\_get HCA

ib\_systemInfo

<details>

<summary>Explanation</summary>

Status of `ibaddr`

* **Outdated?** Yes, for modern RoCE and complex InfiniBand fabrics. It primarily shows the LID range and the default GID of a target port.
* **Replacement:** Use **`ibstat`** for local port information or **`ibnetdiscover`** for a full fabric view.
* **Why use the replacement?** `ibstat` provides a cleaner, more readable view of local LID and GUID information. For network-wide GID discovery, `ibnetdiscover` is the standard for scanning the entire topology to map GUIDs to specific node types and port numbers.&#x20;

<br>

</details>

#### Question 3

**Question text**

What layer does InfiniBand routing use?

Question 3Select one:

Physical Layer

Network Layer :white\_check\_mark:

OSI Layer

Upper Layer

Transport Layer

#### Question 4

What is the purpose of an InfiniBand Router?

Question 4Select one:

Configure InfiniBand subnets

Route traffic between InfiniBand subnets :white\_check\_mark:

Route traffic between InfiniBand subnets, Ethernet, and token ring networks

Optimize traffic patterns

<details>

<summary>Explanation</summary>

An InfiniBand (IB) router connects separate IB subnets to enable scaling beyond 40,000 end-ports, allowing for increased network size, traffic isolation, and management of large-scale HPC or AI fabric. They facilitate communication between different topologies and enhance fault resilience by separating "islands". Key functions and purposes include:

* **Subnet Interconnection:** _Bridges distinct InfiniBand subnets_, enabling seamless communication between them.
* **Scalability:** Facilitates the expansion of InfiniBand fabrics to over 40,000 nodes, which is beyond the limit of a single subnet.
* **Traffic Isolation and Security:** Separates network traffic between subnets, allowing for improved management and security.
* **Global Routing:** Performs routing between subnets using the Global Routing Header (GRH) and Global Identifiers (GIDs).
* **Topology Flexibility:** Connects subnets with different,, or incompatible,, configurations.
* **Performance:** Maintains low latency and high-speed data transfer across the bridged network.&#x20;

</details>

#### Question 5

In a packet header what field is used to route packets across subnets?

Question 5Select one:

System GUID

Node GUID

Route ID

Local ID

Global ID :white\_check\_mark:
