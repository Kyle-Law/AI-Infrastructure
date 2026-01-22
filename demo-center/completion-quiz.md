# Completion Quiz

#### Question 1

Which of the following statements are true? (Select 2)

* Socket programming relies on system calls which uses the OS API.
* RDMA provides better latency and utilization of the hosting machine hardware.
* RDMA cannot coexist with socket programming on the same application.
* With RDMA, the operating system API is used directly with the dedicated hardware, which makes data-transfer faster.

Correct Answer:

* RDMA provides better latency and utilization of the hosting machine hardware.
* Socket programming relies on system calls which uses the OS API.

***

#### Question 2

Select the correct answer regarding Libibverbs:

* Libibverbs is part of the Mellanox OFED driver.
* Verbs API is used as a wrapper for the Socket API.
* Libibverbs is an open-source user space library for RDMA applications.
* RDMA applications doesn’t have to link against Libibverbs, it can work out of the box as long as it has the right hardware connected on the host running the app.

Correct Answer:

* Libibverbs is an open-source user space library for RDMA applications.

***

#### Question 3

Which of the following are objects that are part of the verbs API? (Select 3)

* Work Request
* Work Completion
* Buffer Queue
* Completion Queue

Correct Answer:

* Completion Queue
* Work Request
* Work Completion

***

#### Question 4

Which of the following statements are true? (Select 2)

* Work requests that are posted to Work Queues will be handled by the hardware in the order they were posted.
* QP object contains two Work Queues – for sending and receiving.
* A work request buffer (that was either sent or received) can only be accessed when the work request is marked as outstanding.
* When an application wants to send data, it will post a work request to the Completion Queue and wait for it to be sent to the other side.

Correct Answer:

* QP object contains two Work Queues – for sending and receiving.
* Work requests that are posted to Work Queues will be handled by the hardware in the order they were posted.

***

#### Question 5

Assume a message or several messages were sent by an RDMA application. Which of the following steps are necessary on the receiver side to receive the messages? (Select 3)

* Check for Work Completion along with the status of the operation.
* Create a Work Request and post it on the Receive Queue.
* Create a QP for each expected message sent by the sender side.
* Allocate buffers to store the received messages.

Correct Answer:

* Create a Work Request and post it on the Receive Queue.
* Check for Work Completion along with the status of the operation.
* Allocate buffers to store the received messages.

***

#### Question 6

Assume a message or several messages were sent by an RDMA application. Which of the following steps are necessary on the sender side to send the messages? (Select 3)

* Generate Work Request for each message that is being sent to the other side.
* Resolve the destination app IP address and port and configure the Socket accordingly.
* Check for Work Completion along with the status of the operation for each Work Queue entry.
* Post each Work Request to the Send Queue.

Correct Answer:

* Generate Work Request for each message that is being sent to the other side.
* Post each Work Request to the Send Queue.
* Check for Work Completion along with the status of the operation for each Work Queue entry.

***

#### Question 7

Which of the following statements are true? (Select 2)

* Verbs can only send or receive to registered memory.
* RDMA MM (Memory Manager) is in charge of mapping the physical memory to the virtual memory of the process.
* RDMA Memory registration involves the host OS.
* RDMA allows the application to access any vacant address on the host memory without getting a segmentation fault.

Correct Answer:

* Verbs can only send or receive to registered memory.
* RDMA Memory registration involves the host OS.

***

#### Question 8

Which of the following steps are needed to form RC connection between RDMA applications? (Select 2)

* The receiver side QP needs to be set with the RTR state (Ready To Receive).
* One of the applications has to set the MTU to value of at least 1500.
* Both sides QPs need to be set with the RTS state (Ready To Send).
* Both applications need to create a QP and make sure the other side has the QP address.

Correct Answer:

* Both applications need to create a QP and make sure the other side has the QP address.
* The receiver side QP needs to be set with the RTR state (Ready To Receive).

***

#### Question 9

Which of the following is the correct order of operations that is required to release resources for RDMA applications?

* Call `free()` -> `ibv_close_device` -> `ibv_dereg_mr` -> `ibv_destroy_QP`
* `ibv_destroy_QP` -> `ibv_dereg_mr` -> `ibv_close_device` -> `free()`
* `ibv_dereg_mr` -> `ibv_destroy_QP` -> `free()` -> `ibv_close_device`

Correct Answer:

* `ibv_destroy_QP` and `ibv_destroy_CQ` - to destroy the queue pair and the completion queue respectively.
* `ibv_dereg_mr` – to deregister the memory region used for sending and receiving data.
* If a completion channel was used, `ibv_close_device` is used to destroy it.
* Call `free()` to free the memory used for the buffer and the context itself.

***

#### Question 10

Which of the following are supported RDMA Atomic operations that are part of Libibverbs? (Select 2)

* Compare and swap - compare the current value and if it matches, replace it with a different value.
* Fetch and add - fetch the current value of a number, then we increase it by a different number.
* Increment – Increases the current value by 1.
* Match – check if the current value equals the given value, returns 0 if result is true, 1 otherwise.

Correct Answer:

* Compare and swap - compare the current value and if it matches, replace it with a different value.
* Fetch and add - fetch the current value of a number, then we increase it by a different number.

***

#### Question 11

Which RDMA Libibverbs command can be used to check the completion queue?

* `ibv_poll_cq`
* `ibv_check_status`
* `ibv_post_receive`
* `ibv_post_wr`

Correct Answer:

* `ibv_poll_cq`

***

#### Question 12

Which of the following statements are true? (Select 2)

* In RDMA, data is passed directly to the dedicated hardware (e.g., NVIDIA Adapter) without involving the OS.
* OS is not involved while using RDMA, and does not require any software to be installed on the host OS (e.g., device driver).
* RDMA can be used on any machine, as long as it is running a LINUX based OS.
* There are RDMA operations that go through the operation system.

Correct Answer:

* In RDMA, data is passed directly to the dedicated hardware (e.g., NVIDIA Adapter) without involving the OS.
* There are RDMA operations that go through the operation system.

***

#### Question 13

RDMA CM is used to manage connections for RDMA. Which of the following statements are true? (Select 2)

* RDMA CM is part of the IB verbs library.
* RDMA CM has an event channel to be used for connection establishment events.
* RDMA CM API is designed to be similar to server-client in TCP.
* RDMA CM can be used to automate the data sending and receive process for RDMA apps.

Correct Answer:

* RDMA CM API is designed to be similar to server-client in TCP.
* RDMA CM has an event channel to be used for connection establishment events.

***

#### Question 14

Which of the following statements are true? (Select 2)

* RDMA control operations such as resource allocation or connection establishment typically involve the host OS.
* When sending or receiving data, RDMA is using the socket library to pass the data to the device driver, from which it is being sent to the dedicated hardware.
* Some RDMA operations are not involving the host OS, but there are RDMA operations that go through the OS.
* RDMA programming library is using the same API as the traditional socket API (e.g., `connect()`, `bind()`, `listen()`, `accept()`).

Correct Answer:

* Some RDMA operations are not involving the host OS, but there are RDMA operations that go through the OS.
* RDMA control operations such as resource allocation or connection establishment typically involve the host OS.

***

#### Question 15

Select the correct answer regarding RDMA communication models:

* RDMA is implemented as a two-sided communication model, the sender sends information, and the receiver accepts it and store it in its memory.
* RDMA supports the one-sided communication model, where sender can send data but the receiver does not need to be involved.
* RDMA caches the data in HW buffers and sends it to the other side upon request by using system API calls.
* RDMA doesn’t have to know the remote side address, it can store the information directly in the destination buffers.

Correct Answer:

* RDMA supports the one-sided communication model, where sender can send data but the receiver does not need to be involved.

***

#### Question 16

Which of the following statements are true? (Select 2)

* RDMA uses temporary buffers on both sides and copies data to and from those buffers.
* RDMA uses the “zero-copy” method, which avoids making data copies on the destination host side.
* RDMA is extremely efficient when it comes to small messages, the smaller the message - the faster RDMA will be able to send it.
* RDMA tries to minimize the number of memory copies needed to transfer the data to the destination memory.

Correct Answer:

* RDMA uses the “zero-copy” method, which avoids making data copies on the destination host side.
* RDMA tries to minimize the number of memory copies needed to transfer the data to the destination memory.

***

#### Question 17

What would be the optimal message size to be sent using RDMA?

* RDMA uses “zero copy” which is going to save more time when dealing with large messages.
* Small messages that can fit a single buffer are ideal, which makes it easier to copy from one buffer to another with no re-allocations.
* The message size needs to be at least half of the local memory buffer, so that RDMA can send and receive messages on the same buffer.
* Message size will not affect the overall performance as long as it fits the MTU configured on the physical link connecting the hosts (or host to switch).

Correct Answer:

* RDMA uses “zero copy” which is going to save more time when dealing with large messages.

***

#### Question 18

Which of the following statements are true regarding the RDMA transport layer? (Select 2)

* RDMA transport layer is responsible for determining the destination address of the remote host.
* RDMA transport layer is responsible for determining if a connection is used for a single message or a constant flow of data.
* The transport layer adds the CRC field on each InfiniBand packet, which is used to check if the packet is corrupted.
* RDMA transport layer is responsible for determining if a connection needs to be established for the data transport process.

Correct Answer:

* RDMA transport layer is responsible for determining if a connection needs to be established for the data transport process.
* RDMA transport layer is responsible for determining if a connection is used for a single message or a constant flow of data.

***

#### Question 19

Which of the following statements are true regarding RC vs UD transport?

* RDMA RC transport is much more scalable than RDMA UD transport.
* RDMA UD transport is typically used for client-server applications.
* RDMA RC transport is a reliable connection-oriented transport, it can be compared to TCP in the traditional TCP/IP protocol stack.
* RDMA UD transport is a un-reliable datagram service, it can be compared to UDP in the traditional TCP/IP protocol stack.

Correct Answer:

* RDMA RC transport is a reliable connection-oriented transport, it can be compared to TCP in the traditional TCP/IP protocol stack.
* RDMA UD transport is a un-reliable datagram service, it can be compared to UDP in the traditional TCP/IP protocol stack.

***

#### Question 20

Which of the following are mechanisms to enforce reliability in the message transport process? (Select 2)

* Message numbering to decide which message part needs to be retransmitted.
* “Timeouts” to decide if a message needs to be retransmitted.
* Error messages (notifications) that tells the sender if it needs to retransmit the message.
* Connection manager that queries both side of the connection and able to check that all messages are received.

Correct Answer:

* “Timeouts” to decide if a message needs to be retransmitted.
* Message numbering to decide which message part needs to be retransmitted.
