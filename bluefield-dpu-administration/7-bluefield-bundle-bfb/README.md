# 7 - BlueField Bundle - BFB

Objectives:

* Explain what BFB is and what it's used for
* Check BFB version installed on the DPU
* Upgrade a BFB version on the DPU
* Outline what DPU Firmware is



BFB

* ATF
* UEFI
* OS



Check BFB Version - `sudo bfver`

<figure><img src="../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>



Upgrade BFB Version

1. Download the BFB Image

<figure><img src="../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>



2. Install BFB

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

BF Config File

<figure><img src="../../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

Set default password

<figure><img src="../../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>



3. Verify the new BFB version

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

My Q; why not `sudo bfver` ?

A: It's just a file containing the BFB version



#### BFB Upgrade via BMC



Mgt PC (User requests from here) -> DPU's BMC (Upgrade happen here\_ ->(key exchange protocol - SCP protocol) Server with SSH (File sending to DPU BMC from here)



Key Exchange Configuration

<figure><img src="../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>



Upgrade Command

<figure><img src="../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>



Upgrade status check

<figure><img src="../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>



Upgrading via BMC with Direct SCP

<figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>



Bluefield DPU Firmware

<figure><img src="../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

