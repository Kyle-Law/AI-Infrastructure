# Quiz

### DPU Virtual Switching and Representors

#### Question 1

What does the default configuration of the OVS in BlueField DPU provide?

* Connections between the firmware and the operating system
* Connections between the operating system and the hardware
* Connections between the host and the firmware
* Connections between the host and the DPU and from the host to the outside world ✅

> Note: Upon first boot after installation, the BlueField software typically runs a configuration script (`mlnx_bf_configure`) that sets up a default OVS bridge. This bridge contains ports for the Uplink (p0/p1) and the Host PF representors (pf0hpf/pf1hpf), effectively creating a data path that connects the host server to the DPU's Arm cores and the external network.
>
> <a class="button secondary"></a>

***

#### Question 2

What is the purpose of netdev representors in the DPU?

*   To provide a connection between the virtual switch or application on the Arm cores and the physical function or virtual function on the host side. ✅

    <a class="button secondary"></a>
*   To serve as a virtual port for OVS or other virtual switches running on the Arm cores. ✅

    <a class="button secondary"></a>
*   To configure the embedded switch with rules corresponding to the represented function. ✅

    <a class="button secondary"></a>
* To increase the clock speed of the DPU for better performance

> Note: Netdev representors are the software handles on the DPU (Arm side) that "represent" the PCI functions (PFs/VFs) assigned to the host. They act as the pipe through which traffic is sent to the host and the control channel for offloading hardware rules via technologies like ASAP².
>
> <a class="button secondary"></a><a class="button secondary"></a>

***

#### Question 3

What is the naming convention for the DPU VF representors?

* `p<port_number>`
* `vf<function_number><port_number>`
* `pf<port_number>vf<function_number>` ✅
* `pf<port_number>hpf`

> Note: NVIDIA follows a strict naming hierarchy for representors:
>
> * Uplink: `p0`, `p1`
> * Host Physical Function (HPF): `pf0hpf`, `pf1hpf`
> * Host Virtual Function (VF): `pf0vf0`, `pf0vf1`, etc.

***

#### References & Further Reading

* [NVIDIA Docs: DPU Kernel Representors Model](https://docs.nvidia.com/doca/sdk/dpu-kernel-representors-model/index.html)
* [NVIDIA Docs: Virtual Switch on BlueField DPU](https://docs.nvidia.com/networking/display/bluefielddpuosv385/virtual+switch+on+bluefield+dpu)
* [NVIDIA DOCA: vSwitch and Representors Model User Guide](https://docs.nvidia.com/doca/sdk/Virtual-Switch-on-BlueField/index.html)
