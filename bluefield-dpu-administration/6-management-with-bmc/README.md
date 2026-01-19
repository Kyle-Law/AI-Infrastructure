# 6 - Management with BMC

Objectives

* Explain What's BMC and what it's used for
* Describe what is Redfish
* Use local and remote RedFish tool commands for BMC platform management operations
* Establish an RShim console from BMC to DPU
* Establish a DPU console via BMC SoL



BMC

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>



BMC Access

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>



BMC Support in DPU

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>



Nvidia Firmware Tools (MFT) Package

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

MFT Contains

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>



MFT Service

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>



DPU Device Path

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>



BMC Platform Access

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>



BMC MAC Address

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>



BMC Version

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>



#### Redfish Overview

Redfish Management Protocol

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>



Managing DPU using Redfish

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>



Redfish Protocol Usage Demostration

<figure><img src="../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>



Redfish Protocol Reply Output - Using 'curl'&#x20;

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>



Using Redfish Commands

Create new BMC User

<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

List BMC Users

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

Enable RSHIM via BMC

<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

Check BMC Version

<figure><img src="../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

Additional Redfish Operations

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>



#### RShim from BMC to DPU

Zero Trust Mode

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>



RShim from BMC to DPU

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>



Set an RShim Connection from BMC to DPU

Enable RShim on the BMC

<figure><img src="../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>



Configure the RShim interface

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>



SSH from BMC to DPU via RShim

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>



Enable RShim Service Remotely

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>



#### DPU Console via BMC SoL

Serial Over LAN (SoL)

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>



Get SOL Information

<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>



Connect to SoL - `ssh root@bmc -p 2200`

To Terminate SoL Console - type `~.`

<figure><img src="../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

