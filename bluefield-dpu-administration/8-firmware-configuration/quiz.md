# Quiz

#### Question 1

What controls and manages the configuration of the NIC interfaces in a BlueField DPU in DPU mode?

*   The NIC resources

    <a class="button secondary"></a>
* The Arm processor ✅
*   The ICM

    <a class="button secondary"></a>
* The embedded switch

> Note: In DPU Mode (also known as ECPF mode), the NIC resources and functionality are owned and controlled by the embedded Arm subsystem. All configuration memory (ICM) is allocated by the Arm cores, and the host drivers can only load after the Arm side has completed the NIC initialization.
>
> <a class="button secondary"></a><a class="button secondary"></a>

***

#### Question 2

What is the default operation mode for a BlueField DPU?

* CPU mode
* DPU mode ✅
* NIC mode
* VPI mode

> Note: NVIDIA BlueField DPUs are shipped from the factory in DPU mode by default. In this state, the DPU acts as an independent computer-on-a-card. (Note: The "SuperNIC" variant of BlueField-3 is an exception and typically ships in NIC mode).
>
> <a class="button secondary"></a><a class="button secondary"></a>

***

#### Question 3

What does Single Root IO Virtualization (SR-IOV) technology do?

* Limits the number of times a physical PCIe device can present itself through the PCIe bus
* Increases the speed of the PCIe bus
* Decreases the number of physical PCIe devices
*   Virtualizes a physical PCIe device ✅

    <a class="button secondary"></a>

> Note: SR-IOV allows a single physical PCIe resource (a Physical Function or PF) to appear as multiple separate logical devices (called Virtual Functions or VFs). This allows multiple Virtual Machines to share a single physical NIC with near-native performance by bypassing the hypervisor's software bridge.
>
> <a class="button secondary"></a><a class="button secondary"></a>

***

#### References & Further Reading

* [NVIDIA Docs: BlueField Modes of Operation](https://docs.nvidia.com/networking/display/bluefielddpuosv470/modes+of+operation)
* [NVIDIA Docs: Single Root I/O Virtualization (SR-IOV)](https://docs.nvidia.com/networking/display/mlnxenv23106161lts/Single-Root-IO-Virtualization-\(SR-IOV\))
* [NVIDIA DOCA: DPU Architecture Overview](https://developer.nvidia.com/networking/doca)
