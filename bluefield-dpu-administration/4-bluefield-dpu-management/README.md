# 4 - BlueField DPU Management

#### Objectives

* List the DOCA software components
* Recall the DOCA installation methods for a Linux system
* Perform DOCA installation on hte host and on the DPU



#### DOCA software architecture

DOCA - a complete software environment that includes host-side software and DPU-side software

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>



#### DOCA OS Profiles

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>





#### DOCA OS Profiles Compatibilitiy



<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>



#### Installing DOCA on the Host

Installation Guidelines

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

[https://docs.nvidia.com/doca/sdk/doca-installation-guide-for-linux/index.html](https://docs.nvidia.com/doca/sdk/doca-installation-guide-for-linux/index.html)<br>

Uninstallating older DOCA version from the host

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>



Unpack the DOCA repo

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>



Prerequisite: Install RSHIM

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>



Installing DOCA packages

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>



Verify Installation

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>



List DOCA packages installed on the host

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

1. `wget` to download dev package
2. `dpkg -i` to install package
3. `apt-get update` to update package index files inthe system
4. `apt-get -y install doca-all` to install doca update and all dependenties



BlueField Bundle (BFB)



BD mgt

BlueField Networking Platform Management Software

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>



BlueField Networking Platform MAC Address

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>



OOB Management

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>



