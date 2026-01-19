# Quiz

### DPU Installation and Software Management

#### Question 1

What should you specify after the `–bfb` argument when running the BFB installation script?

* The host with the DPU
* The `rshim` interface to use to install the BFB
* The file name of the BlueField Bundle ✅
* The installation script location

> Note: The `bfb-install` command uses the `--bfb` (or `-b`) flag to point to the specific `.bfb` (BlueField Bundle) image file that contains the OS, firmware, and DOCA packages to be pushed to the DPU.

***

#### Question 2

What file contains the BFB version?

* `/etc/os-release` on the BlueField
* `/etc/mlnx-release` on the BlueField ✅
* `/etc/mlnx-release` on the host where the BlueField is installed
* `/etc/os-release` on the host where the BlueField is installed

> Note: While `/etc/os-release` provides standard Linux distribution info (like Ubuntu or CentOS), NVIDIA-specific versioning (DOCA, BSP, and BFB versions) is stored in the `/etc/mlnx-release` file located specifically on the BlueField ARM OS itself.

***

#### References & Further Reading

* [NVIDIA Docs: Deploying BlueField Software Using BFB from Host](https://docs.nvidia.com/networking/display/bluefielddpuosv470/deploying+bluefield+software+using+bfb+from+host)
* [NVIDIA BFB Image Installation Guide](https://docs.nvidia.com/doca/sdk/bf-bundle-installation-and-upgrade/index.html)
* [NVIDIA BlueField-3 DPU Controller User Manual](https://www.google.com/search?q=https://docs.nvidia.com/networking/display/bluefield3bmc)
