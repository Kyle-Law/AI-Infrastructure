# Final Quiz

#### Section 1: DPU Fundamentals & Architecture

Question 1 What are the two key functions of a DPU? (Select two options)

* Offload, accelerate and isolate the infrastructure services from the host CPU. ✅
* It can be programmed to perform automatic data backup to ‘cold’, ‘warm’ and ‘hot’ sites.
* Run cluster job-scheduling and health monitoring tasks.
* Run an organization main database server, to speed up IO.
*   Free up the host CPU to run money-making applications. ✅

    <a class="button secondary"></a>

> Explanation: The Data Processing Unit (DPU) is designed to take over infrastructure tasks (networking, storage, security) from the main CPU. This "offloads" the work, "accelerates" it using specialized hardware, and "isolates" the infrastructure security domain, ultimately freeing up the CPU to run the actual business applications ("money-making applications").
>
> <a class="button secondary"></a><a class="button secondary"></a>

Question 2 Match each chip type with its primary function.

*   GPU: Used for accelerated computing, executing parallel processing on a massive scale that is essential for graphics and artificial intelligence applications.

    <a class="button secondary"></a>
* DPU: Used for data-intensive functions, such as communication processing, compression, and encryption.
* CPU: Used for general application processing, particularly those that are single threaded.

> Explanation:
>
> * CPU: The general-purpose "brain" suitable for serial processing.
> *   GPU: The parallel processor ideal for AI and Graphics.
>
>     <a class="button secondary"></a>
> *   DPU: The infrastructure processor for moving and securing data.
>
>     <a class="button secondary"></a>

Question 3 Which option best describes how a DPU assists in offloading networking infrastructure services in a software-defined data center?

* It offers dedicated hardware for network and storage acceleration, enabling the CPU to offload routine tasks to the DPU. ✅
* It routes east-west network traffic to specific switches, allowing the datacenter network to focus on incoming business-logic requests.
* It isolates micro-services to run on a subset of servers that are separated from the main SDN of the datacenter.
* It separates traffic from micro-services into a different sub-network, freeing up the main network to handle traffic from key business applications.

> Explanation: The DPU contains specific hardware accelerators (like packet steering and encryption engines) that handle the heavy lifting of network traffic processing, removing this burden from the server's main CPU.

Question 4 Which of the following storage acceleration features is NOT offered by the BlueField DPU?

* SHA-based de-duplication.
* API access to Object Storage. ✅
* Storage emulation.
* Support for RDMA over IP
*   Encryption and decryption for data at-rest and in-flight.

    <a class="button secondary"></a>

> Explanation: While the DPU can accelerate encryption, RDMA, and storage emulation (like NVMe-oF), "API access to Object Storage" is typically a software-layer function of the application or storage controller, not a native hardware acceleration feature of the DPU chip itself.

Question 5 Which of the following statements correctly identify the key differences between the BlueField DPU Mode and NIC Mode? (Select two options)

* In CPU Mode, the DPU's Arm subsystem is entirely controlled by the Host OS.
* DPU mode is designed for InfiniBand communication, while CPU mode is targeted to Ethernet.
*   In DPU Mode, the NIC resources and functionality are controlled by the Arm OS ✅

    <a class="button secondary"></a>
* In NIC Mode, the network control path is managed by applications running on the Host OS. ✅
* DPU mode is recommended for legacy infrastructures.

> Explanation:
>
> * DPU Mode: The Arm cores on the DPU own the card. They boot first and control the network functions.
> *   NIC Mode: The DPU behaves like a standard network card; the host computer's OS manages the network drivers.
>
>     <a class="button secondary"></a>

***

#### Section 2: Storage & SNAP Technology

Question 6 Choose three statements that demonstrate how the BlueField DPU SNAP technology accelerates elastic composable storage: (Select three options)

* It logically presents network storage as a local drive. ✅
* It eliminates the requirement for the Host OS to use special drivers to connect to local or remote storage devices. ✅
*   It enables hardware-accelerated virtualization of NVMe storage. ✅

    <a class="button secondary"></a>
* It performs automatic data backup to ”cold” “warm” and “hot” sites.
*   It encrypts and decrypts all the at-rest data.

    <a class="button secondary"></a>

> Explanation: SNAP (Software-Defined Network Accelerated Processing) allows remote storage (over the network) to appear to the host OS as if it were a local physical NVMe drive. This requires no special drivers on the host because the DPU handles the translation entirely.

***

#### Section 3: DOCA Installation & Management

Question 7 Based on the following command output, what initial action should a system administrator take to install the most recent DOCA version for their host?

* Upgrade the DOCA version on the DPU.
* Uninstall the current DOCA version from the host.
* Locate and download the most recent DOCA version from the NVIDIA website. ✅
* Obtain a DOCA license from the NVIDIA website.

> Explanation: The first step in a host-side installation is always acquiring the correct software package (deb/rpm) for the specific OS from the official vendor source.

Question 8 Which two statements are true regarding DOCA version upgrade for the DPU.

* Upgrading the DOCA local repository package is the recommended method for DOCA upgrade.
* Upgrading through BFB performs a full DOCA image upgrade. ✅
* BFB upgrade is the recommended method for DOCA upgrade. ✅
* Upgrading the DOCA local repository package performs a full DOCA image upgrade.

> Explanation: The BFB (BlueField Bundle) is the complete image containing the Bootloader, Operating System, Firmware, and DOCA software. Flashing the BFB is the standard way to ensure a clean, full system upgrade on the DPU.
>
> <a class="button secondary"></a>

***

#### Section 4: Connectivity (RShim & OOB)

Question 9 How does RShim connect to the BlueField DPU? Select the best answer:

* Through a USB port.
* Using the system's PCIe interface. ✅
* Over a network connection.
* Through a serial cable.

> Explanation: RShim (Remote Shim) drivers create a virtual communication channel between the Host and the DPU over the PCIe bus, allowing the host to access the DPU's console even if the DPU's network is down.
>
> <a class="button secondary"></a>

Question 10 Based on the following command output, what would be the MAC address of the OOB interface? _(Assuming a standard Base MAC scenario provided in typical training)_

* 9c:63:c0:1c:94:ee
* 9c:63:c0:1c:94:ec
* 9c:63:c0:1c:94:eb
* 9c:63:c0:1c:94:ef ✅

> Explanation: On BlueField DPUs, the OOB (Out-of-Band) management MAC address is derived from the Base MAC address printed on the label. The calculation is often Base MAC + (Number of Ports) + Offset. In many BlueField-2 examples, the OOB MAC ends in a higher digit than the port MACs (e.g., Base `ec` -> OOB `ef`).

Question 11 What command is used on an Ubuntu-based host to check the status of the RShim driver?

* `dmesg | grep rshim`
* `lspci -vvv | grep RShim`
* `systemctl status rshim` ✅
*   `rshim status`

    <a class="button secondary"></a>

> Explanation: RShim runs as a system service on Linux. The standard command to check any service status in Ubuntu/Systemd is `systemctl status <service_name>`.
>
> <a class="button secondary"></a>

***

#### Section 5: Hardware Management (BMC & Firmware)

Question 12 What role does the BMC serve on a DPU board?

* To act as a communication gateway.
* To supply the required power to the DPU board.
* To execute high-speed calculations.
* To manage and monitor the subsystem of the DPU board. ✅

> Explanation: The BMC (Baseboard Management Controller) is a specialized chip responsible for physical health monitoring (temperature, power) and remote management (rebooting, firmware updates) of the DPU card itself.

Question 13 What is the purpose of the Arm Trusted Firmware (ATF) in the BFB file used to boot the BlueField DPU?

* To manage the hardware and software resources of the BlueField DPU.
* To provide a reference implementation of Arm processor boot flow. ✅
* To store the BlueField DPU configuration settings and user data.
* To define the interface between the operating system and the system’s firmware.

> Explanation: ATF provides the secure boot environment. It is the very first code that runs on the Arm cores to initialize the secure world before passing control to the UEFI or Operating System.

Question 14 What protocol is preferred to be used to control the DPU via BMC?

* Redfish ✅
* ipmi
* sntp
* snmp

> Explanation: While IPMI is an older standard, Redfish is the modern, RESTful API standard preferred for managing server hardware and DPUs because it is more secure, scalable, and easier to automate.
>
> <a class="button secondary"></a>

Question 15 What is the role of the BlueField DPU firmware?

* To manage the DPU’s hardware and software resources.
* To store the DPU’s configuration settings and user data.
* To provide a reference implementation of the boot flow for Arm processors.
* To interact with the hardware and presenting an interface for the operating system to access the hardware's resources. ✅

> Explanation: Firmware sits between the hardware and the OS/Driver. It handles low-level hardware initialization and exposes the capabilities of the device (like NIC ports) to the software layers.

***

#### Section 6: Virtualization & Telemetry

Question 16 Based on the following command output, in which mode the DPU is operating? _(Assuming standard `mlxconfig` output showing INTERNAL\_CPU\_MODEL=EMBEDDED\_CPU(1))_

* CPU mode
* DPU mode ✅
* Host mode
* NIC mode

> Explanation: In `mlxconfig`, if the configuration shows `INTERNAL_CPU_MODEL` set to `EMBEDDED_CPU` (or value 1), it indicates the Arm cores are enabled and controlling the device, which is DPU Mode. If it were 0 (DISABLED), it would be NIC Mode.

Question 17 What command can you use to query the configuration parameter values of the BlueField DPU when verifying if it's set to function in NIC mode?

* Using the 'mlxconfig' command. ✅
* Using the 'dpuconfig' command.
* Using the 'bfconfig' command.
* Using the 'dpumode' command.

> Explanation: `mlxconfig` is the standard NVIDIA utility for querying and setting non-volatile firmware configurations (TLV parameters) on Mellanox/NVIDIA networking devices.
>
> <a class="button secondary"></a>

Question 18 Which of the following statements best describes SR-IOV?

*   SR-IOV is a specification that permits a PCIe device to appear as a single PCIe device.

    <a class="button secondary"></a>
*   SR-IOV allows for better bandwidth utilization and increased VM density on hosts, among other benefits. ✅

    <a class="button secondary"></a>
* SR-IOV introduces solely the idea of physical functions (PFs).
* A VF represents a physical instance of the network adapter.

> Explanation: Single Root I/O Virtualization (SR-IOV) allows one physical PCIe device to appear as multiple separate virtual devices (Virtual Functions). This allows Virtual Machines to bypass the hypervisor switch and talk directly to the hardware, increasing efficiency and density.
>
> <a class="button secondary"></a>

Question 19 What purpose do ‘netdev’ representors fulfill in the BlueField DPU? _(Note: Multiple options were arguably correct in the previous set, but this option covers the data path aspect best)_

*   To serve as the virtual ports being connected to OVS or any other virtual switch running on the Arm cores.

    <a class="button secondary"></a>
* To serve as the channel to configure the embedded switch with rules to the corresponding represented function.
*   To serve as the tunnel to pass traffic for the virtual switch or application running on the Arm cores to the relevant PF or VF on the host side. ✅

    <a class="button secondary"></a>

> Explanation: A "representor" is a network interface on the DPU side that corresponds to a function (PF or VF) on the Host side. Packets sent into the representor arrive at the Host; packets sent from the Host arrive at the representor.

Question 20 Which of the following are common uses for SFs (Sub-Functions) when it comes to Arm processors and external communication? (Select two correct answers)

* As a type of storage device.
* As an interface for communication between the Arm processor and external hosts, such as RoCE for SNAP. ✅
* As an encryption protocol.
* As a means of internal communication within the Arm processor. ✅

> Explanation: Sub-Functions (SFs) are lightweight virtual functions. They are used to create scalable interfaces for containers/services running _on the DPU itself_ (internal communication) or to expose services like storage (SNAP) to external entities.
>
> <a class="button secondary"></a>

Question 21 Which of the following best describes the main purpose function of the DOCA BlueMan service?

* To serve as a telemetry and visualization tool for a single Bluefield DPU system. ✅
* To serve as a monitoring tool for gaining visibility into all BlueField DPUs running in a datacenter.
* To serve as a graphical interface (GUI) for configuring BlueField DPU parameters.
* To serve as a graphical user interface (GUI) for developing applications that can run directly on the DPU.

> Explanation: DOCA BlueMan is a "one-box" dashboard. It runs on the DPU and provides a web GUI to view the health, versioning, and status of _that specific_ DPU.

Question 22 How is data on the DPU made accessible through the DOCA BlueMan service? Select the best answer.

* Via the DOCA Telemetry Service (DTS). ✅
* Via a lightweight database operating in the DPU server.
* Via Linux dump files.
* Via system logs.

> Explanation: BlueMan is just the frontend visualization. The backend engine that actually collects the counters, temperature, and status data is the DOCA Telemetry Service (DTS).
