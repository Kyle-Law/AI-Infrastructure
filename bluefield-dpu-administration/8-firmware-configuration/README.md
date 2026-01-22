# 8 - Firmware Configuration



> This unit covers BlueField DPU modes of operation - DPU mode (Embedded Mode) and NIC mode, detailing how to switch between them using specific commands. The unit also covers changing link types between InfiniBand and Ethernet for VPI-supporting DPUs, and explains SR-IOV technology for network virtualization.

Outline

* Configuration DPU Opereation Mode - NIC / DPU Mode
* Configuring LInk Type to Inifiniband / Ethernet
* Enabling SR-IOV



Objectives:

* Describe BD opeartion modes
* Change the DPU operation modes - NIC and DPU
* Switch the BD to work in Embedded mode
* Change the link type to Infiniband / Ethernet
* Enable SR-IOV and set the number of VFs



BlueField DPU Modes of Opeartions

Different modes for specific needs of org and workloads

<figure><img src="../../.gitbook/assets/image (55) (1).png" alt=""><figcaption></figcaption></figure>



#### Configuring NIC mode

Identifying the DPU ID

<figure><img src="../../.gitbook/assets/image (56) (1).png" alt=""><figcaption></figcaption></figure>



Default DPU Operation Mode

Display configuration param values

<figure><img src="../../.gitbook/assets/image (57) (1).png" alt=""><figcaption></figcaption></figure>



#### Configuring NIC Mode

<figure><img src="../../.gitbook/assets/image (58) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (59) (1).png" alt=""><figcaption></figcaption></figure>



#### Configuring NIC Mode with a Multi-line Command

<figure><img src="../../.gitbook/assets/image (60) (1).png" alt=""><figcaption></figcaption></figure>



#### Changing to NIC Mode

Reset the Firmware

<figure><img src="../../.gitbook/assets/image (61) (1).png" alt=""><figcaption></figcaption></figure>



#### Verifying NIC Operation Mode

<figure><img src="../../.gitbook/assets/image (62) (1).png" alt=""><figcaption></figcaption></figure>



#### Configuring DPU Mode

<figure><img src="../../.gitbook/assets/image (65) (1).png" alt=""><figcaption></figcaption></figure>



#### Verifying DPU Operation Mode

Display param values after power cycle

<figure><img src="../../.gitbook/assets/image (64) (1).png" alt=""><figcaption></figcaption></figure>



#### Change Link Type to Infiniband / Ethernet

VPI Supporting DPUs

<figure><img src="../../.gitbook/assets/image (66) (1).png" alt=""><figcaption></figcaption></figure>



Checking Link Type

<figure><img src="../../.gitbook/assets/image (67) (1).png" alt=""><figcaption></figcaption></figure>



Change Link Type to Infiniband / Ethernet (For VPI DPUs)

<figure><img src="../../.gitbook/assets/image (68) (1).png" alt=""><figcaption></figcaption></figure>



#### SR-IOV

<figure><img src="../../.gitbook/assets/image (69) (1).png" alt=""><figcaption></figcaption></figure>



Default SR-IOV Settings

<figure><img src="../../.gitbook/assets/image (70) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (71) (1).png" alt=""><figcaption></figcaption></figure>



#### Verifying SR-IOV Settings

<figure><img src="../../.gitbook/assets/image (72) (1).png" alt=""><figcaption></figcaption></figure>



