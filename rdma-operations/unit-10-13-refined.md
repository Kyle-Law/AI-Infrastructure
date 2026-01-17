# Unit 10 - 13 (Refined)

### Unit 10: RDMA Send/Receive (Two-Sided)

The Send/Receive model is "two-sided" because both the sender and receiver’s software must be actively involved in the transaction.

* The Workflow:
  1. Receiver Preparation: The receiver must be ready _before_ the data arrives. It posts a Receive Request to its Receive Queue, providing a buffer to hold incoming data.
  2. Sender Posting: The sender creates a Work Request (WR), posts it to the Send Queue as a Work Queue Entry (WQE), pointing to the data to be sent.
  3. Transmission: The hardware (RNIC) sees the WQE and pushes the data "over the wire."
  4. Completion: \* In Reliable Transport, the receiver hardware sends an Acknowledgment (ACK) back to the sender.
     * Both sides’ hardware generate a Completion Queue Entry (CQE).
     * Software polls the Completion Queue (CQ) to confirm the operation was successful.

***

### Unit 11: RDMA Write (One-Sided)

RDMA Write allows a sender to direct data into a specific memory location on the remote host without involving the remote host's CPU.

* Key Characteristics:
  * One-Sided: The receiver's software is completely unaware that data is being written.
  * Notification: The sender receives a completion notification, but the receiver usually does not (unless "Write with Immediate" is used).

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Hardware Control: When data arrives, the receiver’s hardware checks Memory Registration (permissions). If valid, it writes the data directly to the specified address.\
<br>

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



***

### Unit 12: RDMA Read (One-Sided)

RDMA Read allows a sender to pull data from a remote machine’s memory.

* The Workflow:
  1. The Sender initiates a request containing the remote memory address and the size of the data it wants to pull.
  2. The Receiver’s Hardware receives the request, validates memory permissions, reads the data from its local RAM, and sends it back over the wire.
  3. The Sender receives the data and places it into its local memory.

***

### Unit 13: Atomic Operations

Atomic operations allow for "Read-Modify-Write" sequences that are guaranteed to be completed by the hardware without interruption from other processes.

* Common Types:
  * Fetch & Add: Reads a value from remote memory and adds a specified value to it in one uninterruptible step.
  * Compare & Swap (CAS): Checks if the remote value matches a "target." If it matches, it replaces it with a "new" value.
* The "Soup" Analogy:
  * The Problem: You taste the soup (Read), realize it needs salt, and go to get salt. Meanwhile, your roommate tastes it (Read) and also goes for salt. You both add salt, and the soup is ruined (Race Condition).
  * The Atomic Solution: You "Taste-and-Add-Salt" in one single, locked action so no one can intervene between the taste and the pour.

***

### Unit 13: Knowledge Check Answers

Question 1: In RDMA read, where is the data to be read stored?

> Answer: On the receiver’s memory.

Question 2: In RDMA write, which of the following is sent from the Sender to the Receiver? (Select two)

> Answer: > 1. The data 2. The memory address it must be written to _(Note: The local address and completion ACKs are handled locally or by hardware, but the payload and destination address must travel over the wire.)_

Question 3: Why are atomic operations needed?

> Answer: They prevent interruption during sets of operations.

#### RDMA Operations Comparison Table

| **Feature**           | **Send/Receive**                    | **RDMA Write**                      | **RDMA Read**                       | **Atomic Operations**      |
| --------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- | -------------------------- |
| Type                  | Two-Sided                           | One-Sided                           | One-Sided                           | One-Sided                  |
| Initiator             | Sender                              | Sender                              | Sender (Requester)                  | Sender (Requester)         |
| Remote CPU Involved?  | Yes (must post receive)             | No                                  | No                                  | No                         |
| Who provides Address? | Receiver                            | Sender                              | Sender                              | Sender                     |
| Data Movement         | Sender $$ $\rightarrow$ $$ Receiver | Sender $$ $\rightarrow$ $$ Receiver | Receiver $$ $\rightarrow$ $$ Sender | Bidirectional (Fetch/Swap) |
| Common Use Case       | Control messages                    | Large data transfers                | Database queries                    | Distributed locks/counters |
