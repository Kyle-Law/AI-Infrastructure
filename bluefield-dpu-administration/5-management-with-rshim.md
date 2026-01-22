# 5 - Management with RShim

Agenda

* RShim overview
* RShim Service
* Conencting to the DPU from the Host RShim Console, RShim Network Interface
* DPU Software Reset with RShim
* Multiple DPUs on a Host



Objectives:

* Enable, disable the RShim service and check its status
* Connect to the DPU via the RShim console or the RShim network interface
* Perform a DPU software rseet with RShim
* Describe RShim Support for multiple DPUs



RShim Service Status

<figure><img src="../.gitbook/assets/image (14) (1).png" alt=""><figcaption></figcaption></figure>



Start/Stop the RShim Service

<figure><img src="../.gitbook/assets/image (15) (1).png" alt=""><figcaption></figcaption></figure>



Starting the RShim Service on Host Startup

<figure><img src="../.gitbook/assets/image (16) (1).png" alt=""><figcaption></figcaption></figure>



#### Connecting to the DPU from the Host

Connecting to the BlueField DPU

<figure><img src="../.gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure>



Connecting to the DPU via the RShim Console

<figure><img src="../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>



RShim Network Interface

<figure><img src="../.gitbook/assets/image (19) (1).png" alt=""><figcaption></figcaption></figure>

Configuring the Host RShim Network Interface

Ubuntu OS

<figure><img src="../.gitbook/assets/image (20) (1).png" alt=""><figcaption></figcaption></figure>



CentOS

<figure><img src="../.gitbook/assets/image (21) (1).png" alt=""><figcaption></figcaption></figure>

Connecting to BlueField DPU via SSH

<figure><img src="../.gitbook/assets/image (22) (1).png" alt=""><figcaption></figcaption></figure>



Login to BlueField DPU via RShim Console

1. Connect to the host where the DPU is installed
2. Verify RShim Service is running - `systemctl status rshim`
3. Open a terminal session to the DPU using minicom or screen - `minicom -D /dev/rshim0/console`
4. creds: ubuntu ubuntu
5. DPU CLI prompt appears



DPU Software reset with RShim

DPU Software reset

<figure><img src="../.gitbook/assets/image (23) (1).png" alt=""><figcaption></figcaption></figure>



RShim support for multiple DPUs

<figure><img src="../.gitbook/assets/image (24) (1).png" alt=""><figcaption></figcaption></figure>



