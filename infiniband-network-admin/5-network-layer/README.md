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



GRH contains GID - a 128-bit field used to identify a single end port or a multicast group



Default GID

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>



OFED Commands

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



Note: the commands are outdated<br>

In 2026, **`ibv_devices`** and **`ibaddr`** are considered legacy utilities. While they may still function in some environments for backward compatibility, they have been superseded by more comprehensive tools within the **MLNX\_OFED** (now transitioning to **DOCA-OFED**) and **rdma-core** stacks. Status of `ibv_devices`

* **Outdated?** Yes. It is a very basic utility that only lists device names and their Node GUIDs.
* **Replacement:** Use **`ibv_devinfo -l`** to list device names or **`ibv_devinfo`** (without flags) for a summary.
* **Why use the replacement?** `ibv_devinfo` provides significantly more detail, including firmware versions, port states, and active MTUs, which are critical for debugging GID-related issues.&#x20;

Status of `ibaddr`

* **Outdated?** Yes, for modern RoCE and complex InfiniBand fabrics. It primarily shows the LID range and the default GID of a target port.
* **Replacement:** Use **`ibstat`** for local port information or **`ibnetdiscover`** for a full fabric view.
* **Why use the replacement?** `ibstat` provides a cleaner, more readable view of local LID and GUID information. For network-wide GID discovery, `ibnetdiscover` is the standard for scanning the entire topology to map GUIDs to specific node types and port numbers.&#x20;

Recommended 2026 WorkflowTo locate and verify GIDs effectively in current environments, prioritize these commands:

1. **`show_gids`**: Still the best for quickly viewing the local GID table, especially for RoCE v1/v2 differentiation.
2. **`ibv_devinfo -v`**: The standard for a deep-dive into device capabilities and full GID tables.
3. **`ibstat`**: The go-to for checking if a port is `ACTIVE` and seeing its base GUID.
4. **`ibnetdiscover`**: Use this to map the fabric if you are trying to locate GIDs for remote nodes.&#x20;

