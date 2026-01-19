# Quiz

### DPU Networking and Software Architecture

#### Question 1

How is the MAC address for the OOB interface determined?

* By subtracting 1 from the base MAC address
* By adding the number of MAC addresses being used (starting from 0) to the base MAC address, then subtracting 1
* By adding the number of MAC addresses being used (starting from 0) to the base MAC address, then subtracting 3 ✅
* By adding the number of MAC addresses being used (starting from 0) to the base MAC address, then subtracting 2

> Note: NVIDIA BlueField DPUs use a specific offset logic derived from the Base MAC (the one printed on the label). The OOB (Out-of-Band) management interface typically follows a calculation where the total number of allocated MACs is added to the base, followed by a fixed subtraction (in this case, 3) to land on the specific OOB address.

***

#### Question 2

Where is the DOCA framework installed?

* Only on the host system
* Only on the DPU
* Exclusively on external network devices
* On both the host and the DPU ✅

> Note: DOCA (Data-Center-on-a-Chip Architecture) is a distributed framework. The DOCA SDK/Runtime is installed on the DPU (ARM side) to run offloaded services, while DOCA-Host components are installed on the host (x86 side) to allow the host applications to communicate with and control the DPU via the drivers and communication channels.

***

#### Question 3

What is the purpose of the BFB (BlueField Bundle) on BlueField?

* To boot the BlueField Networking platform and include DOCA packages ✅
* To exclusively manage the PCIe switch and fabric mesh operations
* To manage network traffic and optimize storage performance
* To handle only the system level cache and controllers

> Note: The BFB is the "all-in-one" image for the DPU. It contains the bootloader (ATF/UEFI), the operating system (typically Ubuntu or CentOS for ARM), and the pre-integrated DOCA libraries and drivers required to initialize the DPU into a functional state.

***

#### References & Further Reading

* [NVIDIA Docs: Finding the MAC on the DPU](https://docs.nvidia.com/networking/display/bluefield2dpuenug/finding+the+mac+on+the+dpu)
* [NVIDIA DOCA: Getting Started Guide](https://developer.nvidia.com/networking/doca/getting-started)
* [NVIDIA Docs: BlueField Bundle (BFB) Installation](https://docs.nvidia.com/networking/display/bluefieldbsp4120/types+and+methods+of+updating+bluefield+software+image)
