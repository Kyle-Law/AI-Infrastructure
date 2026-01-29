# Quiz

What are the main responsibilities of the Upper Layer?

Question 1Select one or more:

Software Transport Verbs :white\_check\_mark:

Transport service types

Management Service protocols :white\_check\_mark:

Upper Layer protocols :white\_check\_mark:

Segmentation and reassembly

#### Question 2

**Question text**

What services make up the management service protocols?

Question 2Select one or more:

Smadmin

Subnet Management Interface :white\_check\_mark:

Application Interface

Message Processing Interface

General Services Interface :white\_check\_mark:

<details>

<summary>Explanation</summary>

* Subnet Management Interface (SMI): This interface is used by the Subnet Manager (SM) to send and receive Subnet Management Packets (SMPs). It is responsible for discovering the topology and configuring switches and channel adapters.
* General Services Interface (GSI): This interface handles all management traffic that isn't strictly subnet management. This includes performance monitoring, connection management, and device management through General Services Agents (GSAs)

| **Interface** | **Purpose**                                              | **Common Agent/Manager**                      |
| ------------- | -------------------------------------------------------- | --------------------------------------------- |
| SMI           | Fabric setup, routing, and topology discovery.           | Subnet Manager (SM)                           |
| GSI           | Performance monitoring, I/O management, and diagnostics. | Performance Manager (PM), Device Manager (DM) |

</details>

#### Question 3

Your organization is considering moving a latency-sensitive HPC application to their InfiniBand network.  What is the best Upper Layer protocol to suggest for this application?

Question 3Select one:

NFS-RDMA

Sockets Direct Protocol (SDP)

IP over InfiniBand (IPoIB)

Message Processing Interface (MPI) :white\_check\_mark:

ISCSI RDMA (iSER)

#### Question 4

**Question text**

What is an example of a Software Transport Verb?

Question 4Select one:

Open Close Exit

Post Send Request :white\_check\_mark:

Write Read Query

Export Import Discard

Push Pull Subscribe

#### Question 5

**Question text**

What is a Software Transport Verb?

Question 5 Select one:

Verbs enable the processing of Natural Language Processing (NLP) network data

Verbs are used for the segmentation and reassembly of payload packets

Verbs are used to enable IP over InfiniBand (IPoIB) functionality

Verbs are a transport layer operation for sending messages across the InfiniBand fabric

Verbs are the application’s software interface to the HCA and the InfiniBand fabric :white\_check\_mark:
