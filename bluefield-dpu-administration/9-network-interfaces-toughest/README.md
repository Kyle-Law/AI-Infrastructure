# 9 - Network Interfaces (toughest)

> This unit covers BlueField DPU network interfaces, including OOB, RShim, PFs, and VFs. It explains the Kernel Representors Model for mapping host functions to the DPU. It also introduces Open vSwitch (OVS) bridges on the DPU, explaining ASAP² acceleration and default configurations. Students will learn to identify and manage various network interfaces and understand traffic flow through the DPU.



#### Outline

* DPU Network Interfaces
* Kernel representors Model
* DPU Representors (PFs, VFs and SFs)
* DPU OVS Bridges



#### Objectives

* List BlueField DPU network interfaces
* Describe the Kernel Representors Model and how it is used to map host-side physical and virtual functions into the DPU
* Desribe the DPU representors for PFs, VFs, and SFs
* Display the DPU's default OVS bridge configuration



#### Network Interfaces

Bluefield  DPU interfaces

<figure><img src="../../.gitbook/assets/image (85) (1).png" alt=""><figcaption></figcaption></figure>

Kernel Representors Model

<figure><img src="../../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

DPU PFs

Representors for DPU network ports

<figure><img src="../../.gitbook/assets/image (87) (1).png" alt=""><figcaption></figcaption></figure>



#### DPU PFs Representor Example

Representors for DPU network ports example

<figure><img src="../../.gitbook/assets/image (88) (1).png" alt=""><figcaption></figcaption></figure>

Host side PF representor: pf1hpf



#### Host VFs Representors

<figure><img src="../../.gitbook/assets/image (89) (1).png" alt=""><figcaption></figcaption></figure>



#### Host VFs Representors Example

<figure><img src="../../.gitbook/assets/image (90) (1).png" alt=""><figcaption></figcaption></figure>



#### VF Example (3:55)

> TODO: Review this part and record what these does
>
> 3:55

<figure><img src="../../.gitbook/assets/image (92) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (93) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (94) (1).png" alt=""><figcaption></figcaption></figure>

Connect to the DPU

<figure><img src="../../.gitbook/assets/image (95) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (96) (1).png" alt=""><figcaption></figcaption></figure>



#### Scalable Functions (SFs)

<figure><img src="../../.gitbook/assets/image (97) (1).png" alt=""><figcaption></figcaption></figure>

SF Representors

<figure><img src="../../.gitbook/assets/image (98) (1).png" alt=""><figcaption></figcaption></figure>

SFs Representors Example

<figure><img src="../../.gitbook/assets/image (99) (1).png" alt=""><figcaption></figcaption></figure>



Traffic Flow via the DPU

<figure><img src="../../.gitbook/assets/image (100) (1).png" alt=""><figcaption></figcaption></figure>



#### DPU OVS Bridges

<figure><img src="../../.gitbook/assets/image (101) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (102) (1).png" alt=""><figcaption></figcaption></figure>

OVS Flavors

<figure><img src="../../.gitbook/assets/image (103) (1).png" alt=""><figcaption></figcaption></figure>



#### DPU OVS Bridges

<figure><img src="../../.gitbook/assets/image (104) (1).png" alt=""><figcaption></figcaption></figure>



#### DPU OVS Default Configuration

<figure><img src="../../.gitbook/assets/image (105) (1).png" alt=""><figcaption></figcaption></figure>

