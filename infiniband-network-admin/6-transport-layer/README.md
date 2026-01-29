# 6 - Transport Layer



Base Transport Header (BTH)&#x20;

* present in all packets except RAW datagrams
* specifies the destination QP and indicates the operation code, packet sequence number, and partition



Operation code

* identify if the packet is the first, last, intermediate, or only packet of a message
* specify the operation (Send, RDMA Write, Read, Atomic)



Packet Sequence Number (PSN)

* initialized as part of the communications establishment process and increments each time the QP creates a new packet
* receiving QP tracks the received PSN to determine if it lost a packet
* For reliable service, receiver sends an ACK or NAK packet back to notify the sender



Extended Transport Header (ETH)

* conditionally present depending on the class of service and the operation code
* For reliable datagram service, ETH identifies the EE context that the QP uses to detect missing packets





