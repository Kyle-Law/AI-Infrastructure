# 2 - Intro to InfiniBand Architecture

### Outline

#### InfiniBand Architecture

* InfiniBand Architecture layers
* InfiniBand packet structure and packet flow

#### InfiniBand Management

* The Subnet Manager
* Nodes addressing
* Traffic routing

#### OFED Monitoring Utilities

### Objectives

By the end of this unit, you will be able to:

* List the InfiniBand Architecture layers
* Explain the role of each InfiniBand architecture layer
* Describe the InfiniBand packet structure and packet flow
* Outline OFED Utilities to monitor the subnet



Resources:

Subnet Manager - [https://docs.nvidia.com/networking/display/mlnxosv3111014/subnet+manager](https://docs.nvidia.com/networking/display/mlnxosv3111014/subnet+manager)&#x20;

[https://enterprise-support.nvidia.com/s/article/lrh-and-grh-infiniband-headers#:\~:text=which%20is%20fixed).-,Global%20Route%20Headers,GID%20has%20the%20following%20format:](https://enterprise-support.nvidia.com/s/article/lrh-and-grh-infiniband-headers)&#x20;

[https://www.scribd.com/presentation/882116351/lect16-infiniband](https://www.scribd.com/presentation/882116351/lect16-infiniband) \
[https://www.linkedin.com/pulse/infiniband-header-explained-networking-perspective-akshay-vaidya-bhlyc/](https://www.linkedin.com/pulse/infiniband-header-explained-networking-perspective-akshay-vaidya-bhlyc/)\
[https://quizlet.com/922890960/infiniband-professional-cert-flash-cards/](https://quizlet.com/922890960/infiniband-professional-cert-flash-cards/) (this is pretty good)\
[https://www.linkedin.com/pulse/understanding-nvidia-infiniband-networking-routing-switching-ahmad--tprvf#:\~:text=InfiniBand%20uses%20LID%20routing%20within,manager%20based%20on%20the%20topology.](https://www.linkedin.com/pulse/understanding-nvidia-infiniband-networking-routing-switching-ahmad--tprvf)

[https://developer.nvidia.com/blog/infiniband-multilayered-security-protects-data-centers-and-ai-workloads/#:\~:text=Management%20built%20for%20security%20at,only%20reduced%20by%20authorized%20switches](https://developer.nvidia.com/blog/infiniband-multilayered-security-protects-data-centers-and-ai-workloads/)\
[https://docs.nvidia.com/doca/archive/2-9-4/mad-congestion-control/index.html#](https://docs.nvidia.com/doca/archive/2-9-4/mad-congestion-control/index.html)\
[https://docs.nvidia.com/networking/display/nvidiainfinibandsecurityoverviewandguidelines/security+in+infiniband#](https://docs.nvidia.com/networking/display/nvidiainfinibandsecurityoverviewandguidelines/security+in+infiniband)<br>

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

Note - odd, in video mentioned each layer can be clicked



InfiniBand Data Packet

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

&#x20;

Data Packet Structure

<figure><img src="../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>



InfiniBand Packet Example

<figure><img src="../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>



InfiniBand Packet Flow

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>



#### Intro to InfiniBand Management

Fabric vs. Subnet

<figure><img src="../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>



The Subnet Manager

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

The Master Subnet Manager

<figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>



Subnet Management Elements

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>



InfiniBand Addressing

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>



Packet Forwarding

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>



#### OFED and OFED Utilities

OpenFrabrics Enterprise Distribution (OFED)

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>



InfiniBand Driver Information

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>



HCAs Information

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>



Local InfiniBand Information

<figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>



Verifying Layer 2 Connectivity

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>



Path Tracing

<figure><img src="../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>



