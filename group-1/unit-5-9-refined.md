# Unit 5 - 9 (Refined)

### Unit 5: Introduction to RDMA Verbs

The Verbs API is the software interface used to interact with RDMA-capable hardware (Host Channel Adapters or HCAs).

* Libibverbs: The standard user-space library in Linux. Applications must link against this to bypass the kernel.
* The Performance Philosophy: RDMA aims for Zero-Copy (data goes directly from app memory to wire) and Kernel Bypass (no context switches).
* Architectural Split:
  * Control Path: Used for resource setup (creating QPs, registering memory). High overhead, involves the OS Kernel.
  * Data Path: Used for actual data transfer (Post Send/Recv). Extremely fast, bypasses the OS entirely.

***

### Unit 6 & 7: Core Objects & Data-Path Flow

RDMA operates on an asynchronous queue model. You don't "send data"; you "post a request."

#### 1. The Queue Pair (QP)

The fundamental unit of communication (analogous to a Socket). Each QP contains:

* Send Queue (SQ): For outgoing operations (Send, Write, Read).
* Receive Queue (RQ): To provide buffers for incoming data.

#### 2. Work Requests (WR) and Completions (CQ)

* Work Request (WR): Created by the Software. You "Post" a WR to a queue. It stays outstanding until the hardware finishes.
* Completion Queue (CQ): The "Inbox" for results. Once the HCA finishes a WR, it pushes a Work Completion (WC) into the CQ.
* Buffer Ownership: While a WR is outstanding, the software must not modify the memory buffer. Ownership only returns to the software once a WC is polled from the CQ.

#### 3. Data-Path Flow (Two-Sided vs. One-Sided)

* Two-Sided (Send/Receive): Both sides are involved. The receiver must "post" a buffer to the Receive Queue _before_ the sender sends data.
* One-Sided (RDMA Read/Write): The initiator specifies the remote memory address. The remote CPU is not involved and doesn't even know the transfer happened.

***

### Unit 8: Memory Management & Registration

In RDMA, the HCA (hardware) needs to access RAM directly without asking the CPU for address translations. This requires a process called Memory Registration.

#### The 3 Pillars of a Memory Region (MR)

1. Pinning: The OS "locks" the memory in physical RAM. It cannot be swapped to disk (paging), ensuring the HCA always finds the data at the same physical address.
2. Protection: Defines permissions (Local Read, Local Write, Remote Read, Remote Write).
3. Translation: The HCA creates a mapping from the Virtual Address (used by the app) to the Physical Address (used by hardware).

#### Memory Keys

* L\_Key (Local Key): Used by the local HCA to access its own memory.
* R\_Key (Remote Key): Shared with a remote node so it can perform one-sided (Read/Write) operations on your memory.

***

### Unit 9: Summary Cheat Sheet

| **Object** | **Full Name**    | **Role**                                               |
| ---------- | ---------------- | ------------------------------------------------------ |
| QP         | Queue Pair       | The "Socket" (Send + Receive Queues).                  |
| WR         | Work Request     | The "Command" (Software $$ $\rightarrow$ $$ Hardware). |
| WC         | Work Completion  | The "Receipt" (Hardware $$ $\rightarrow$ $$ Software). |
| CQ         | Completion Queue | The "Container" for Work Completions.                  |
| MR         | Memory Region    | Registered/Pinned memory buffer.                       |
