# Unit 2 - BlueField DPU Use Cases

focus on specific use cases on DPU use cases on ...

breaktrhrough performance for storage ans security

sotrage defined network to imporve performance

accelerating elastic coputing storae

cover how security functino can be solated to henhacne protection



understand the capabilities of the BlueField DPU sofwtare and hardware accelerators

describe featurse of the BleuField DPU that offload network functions

Describe how the BlueField DPU supports different storage acceleration features

List the BlueField DPUs capabilities that isolate critical security functions from the main host



nvidia bluefield dpu... for today ai workload



shifting infra services from cpu to dpu

security and storage tasks

software defined data center



### Offloading Software-Defined Networks (SDN)

explore how dpu sofwtare defined softward acceleration... networkign sotrage security solution

accelerate... cloud, dc, edge

netwokring, dpu provides ... by offloading complex tasks with software defined compute capabilities

cloud antive app - explosive EW network  where between virtual machine and container

microservice architecture - generate intensive data movements primaryily go EW

<figure><img src="../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>



#### SR-IOV

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

trigger many API calls,&#x20;

high throughoutput low latency netowkri sis essential

DPU accelerate softwaree defined dc service&#x20;

from PC centric design to cloud antive server centric

dedicated hardware... cpu focus on app..&#x20;

in a heavily veirtualize server...&#x20;

single root io virtualization - SR-IOV&#x20;

multiple virtual nic, a ...&#x20;

without virtual swithces insigde hypervisor

... mltiple... host as separate resource

reduce CPU load and improve network efficient

SR-IOV... guarantee isolation and better protection

enable multiple virtual instance



#### DOCA

NVIDIA OVS-DOCA

<figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>



### Paths to Multi-Tenant Cloud

> BlueField provides tenant isolation ewith EVPN VXLAN and/or SDN

<figure><img src="../../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

check HBN vs OVN



#### DOCA Platform Framework (DPF) for Telcos

<figure><img src="../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### Virtual Switch Offloading

OVS and OVN acceleration

<figure><img src="../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### How ASAP2 Works



<figure><img src="../../.gitbook/assets/image (8) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### VirtIO-Networking Acceleration

<figure><img src="../../.gitbook/assets/image (9) (1) (1).png" alt=""><figcaption></figcaption></figure>



### Accelerating Elastic Composable Storage



#### Solutions for Efficient Storage

Offloading Storage Infrastructure to the DPU

<figure><img src="../../.gitbook/assets/image (10) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### DPU Hardware Storage Offloads

<figure><img src="../../.gitbook/assets/image (11) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### Storage Emulation with BlueField SNAP

From local storage to emulated storage

<figure><img src="../../.gitbook/assets/image (12) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### BlueField SNAP

<figure><img src="../../.gitbook/assets/image (13) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### Software-Defined Hardware-Accelerated

<figure><img src="../../.gitbook/assets/image (14) (1) (1).png" alt=""><figcaption></figcaption></figure>



### Isolating Security Functions

#### BlueField - The Most Secure DPU

Trust shifts to the DPU

<figure><img src="../../.gitbook/assets/image (15) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### DPU Hardware Security Engines

Accelerates the most common security services

<figure><img src="../../.gitbook/assets/image (16) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### Hardware-Accelerated Encryption



TODO: view the video here - 18:40

ENcrytoion is an important aspect

wherether storage or ...

can quickly consume general purpose cpu cycle

BD proides dedicates acceleration for e and dcrytpion

by moving encryption function down to dpu..

no long cpu

ndpu handle security...

prvdieng..

TLS and motion inline block level at rest encryption

bd offloads crypto operation, freeing up dpu

deep packet inspection

offer string...

instruction detection.. anti virus

pka engine

arm host&#x20;

provide high performance

reducing overhead .. such as HTTP verserver that using TLS

verify operation





#### Summary

* Understand the capabilities of the BlueField DPU software and hardware accelerators
* Describe BD features that offload network functions
* Describe BD. storage acceleration capabiliities
* List BD capabiliiteis that isolate ritical security functions from the main host



