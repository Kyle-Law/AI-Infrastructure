# Unit 5 - 9 (Raw)

Unit 5 - What are verbs?

verbs is the API for RDMA app

means that RDMA app is willing link agains thte verb library

verb api divide into 2 sections - control (including resource allocation... typically involve OS) and Data path (path send and receive data - has to be fast and efficinet)

Verb APi focus on peformance - close as possible to the hadrware - ensure latency bandwith, ...&#x20;

various app - storage, ai, parrallel programming

Libibverbs - app has to link against the library to get RDMA operation going

open source - available to multiple liux distribution

Focus - user space, user level, and libibverbs



Unit 6 - Verbs Objects



most important objects in verb APIs - Requests - Completions - Queues

Requests: request app to the hardware, typically RDMA operation

Completion - copmletion of prev work request - contain status&#x20;

Queue

work queue: object - allows u to post work requests to be completed by the hardware - post multiple work request by thework queue

multiple queue - order is not guaranteed

every work request is considered outstanding until hardware generate work completion - then u know completion and have access to the buffer (if receive buffer)

read by the software

Send Queue: type of work queue that contain send request - indicating it wants to send the buffer in removte destiination

Receive Queue - post buffer to the send queue via receive worke requst - every time data arrive, it'lll buffer... to th ereceive queue

similar to socket, we got QP, receiv eand send queue bound together





Unit 7 - Data-Path Flow

demo -&#x20;

on software level - work request & work completion

verb library level

hardware level - QP & completion queue&#x20;

QP contains send and receive queue

eg. send side - 2 msg - h & wlc



1. \[Software] 2 work requests
2. \[Hardware] post the work requests to send queue - generate completion queue entry



3rd type of RDMA operation - RDMA read - 1-side operation like RDMA write

the data lies on the receive side

on the receive side, dk how much data will arrive

create buffer - create work requests \[Software] -> receive queue \[Hardware] -> pointed to data allocated

once data arrive - hardware place data in mem allocated and generate completion queue

Sofware check competion queue - in the form of work completion - contains status, and additional info





Unit 7 (Test)





Unit 8 - Memory Management

Process -> actual memory

OS is responsible to map process to RAM address space

use rlevel software which are most app almost use virtual memroy .. some virtual memory range is allocated, the reases are vacant

the apps only access allocated memroy

access vacant memory -> segmentation fault

read write ability to execute code

allocate memory -> OS allocate to vacant space

low memory -> comes with the expense of other system



RDMA - special memory allocation - "memory registration"

part of the control path&#x20;

registered memory has 3 properties

1. Protection - range of ...&#x20;
2. Memory Pinning - physical memory is locked in place
3. Tranlation Handle - used to access memory of the hardware itself

Verb can only receive registered memory - bgn of app - used thrughout the run&#x20;

&#x20;locking into the process&#x20;

advantages - best prossible access in terms of altency and presence always happened in RAM







Unit 9 - Recap

3 most important verb objects - queue pairs, completion queues, memory regions

QP - transport endpoint, just liek socket for TCP communication, - synchronized interface for sending and receiving messages&#x20;

send / receive - create work request and post on send queue / receive queue - both are part of the QP

completion queue - a method to notify us if the request is completed

Memory regions - for registered memory - can only S/R mem registered with verb APIs...&#x20;

