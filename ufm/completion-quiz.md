# Completion Quiz

### NVIDIA UFM Certification Practice Quiz

#### Question 1

Which of the following are UFM features? (Select two)

* Network Congestion Analysis ✅
* Real-Time Network Telemetry ✅
* Host CPU offloading
* Compute Node Scheduler

#### Question 2

What are the common installation options for installing UFM Enterprise? (Select two)

* UFM Enterprise is included with the UFM Telemetry package
* Docker Container Installation ✅
* UFM Server cloning
* Software Installation ✅

#### Question 3

How does the UFM traffic map represent congestion and traffic?

* Source and Destination table
* List of all nodes with a display of their current traffic or congestion status
* Divided by tiers (1 to 4): Server to Leaf, Leaf to Spine, Spine to Leaf, Leaf to Server ✅
* All of the above

#### Question 4

Which of the following can be determined using the UFM's network map?

* The level of congestion a particular node is suffering from
* The amount of transmitted/received traffic over a particular link
* Location of all faulty links
* All of the above ✅ (?)

#### Question 5

Which UFM Dashboard display would you visit to see a collection of info, warnings, and alarms per network element category?

* The "Top 5 Congested Switches" display
* The "Traffic Map" display
* The "Inventory" display ✅
* The "Recent Activities" display



#### Question 6

Which of the following would you look at when attempting to analyze congestion? (Select three)

* “Traffic Map” ✅
* “Logical Elements”
* “Top Congested Servers” ✅
* "Top Congested Switches” ✅



#### Question 7

A customer is using a Kubernetes main management system. To gain information about their fabric ports, we may query the UFM using the following URL:

* GET /ufmRest/resources/systems?type=switch
* GET /ufmRest/app/events
* POST /ufmRest/FabricValidation/tests/test\_name
* GET /ufmRest/resources/ports ✅

{% embed url="https://docs.nvidia.com/networking/display/ufmenterpriserestapiv6140/ports+rest+api" %}

## [Ports REST API](https://docs.nvidia.com/networking/display/ufmenterpriserestapiv6140/ports+rest+api)

Description – returns information about all ports in the fabric, ports of a specific system, or all active and external ports in the fabric

* Request URL – GET /ufmRest/resources/ports

#### Question 8

What information is listed under "Device Information" when observing a particular network component? (Select three)

* Topology snapshots associated with the device
* Suggested actions regarding device alarms
* Events and alarms detected on the device ✅
* Device Ports (Physical and Virtual) ✅
* Linked Cables attached to the device's ports and their details ✅

[https://docs.nvidia.com/networking/display/ufmenterpriseumv61914/devices-window#src-4664483667\_DevicesWindow-DeviceInformationTabs](https://docs.nvidia.com/networking/display/ufmenterpriseumv61914/devices-window#src-4664483667_DevicesWindow-DeviceInformationTabs)<br>

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

#### Question 9

Which of the following are types of logs that may be displayed in “UFM Logs” (under “System Health”)? (Select three)

* SM Logs ✅
* UFM Logs ✅
* Switch OS Logs
* ibdiagnet Logs ✅
* Event Logs

{% embed url="https://docs.nvidia.com/networking/display/ufmenterpriseumv61914/ufm-logs-tab" %}

'The logs are categorized into three files according to the activities they record: Event logs, SM logs, and UFM logs.'

#### Question 10

Why would you visit the “UFM Health” tab (under the “System Health” Menu)?

* To determine whether UFM’s functionalities are working properly ✅
* To collate data recorded in the UFM Logs related to alarms or warnings (Event & Alarms(
* To track changes made to the UFM processes, a system error event ( Tracking, version control somewhere)
* All of the above&#x20;

[https://docs.nvidia.com/networking/display/ufmenterpriseumv61914/ufm-health-tab](https://docs.nvidia.com/networking/display/ufmenterpriseumv61914/ufm-health-tab)<br>

#### Question 11

Which of the following operations can be performed in the "IBDiagnet" tab under the "System Health" menu? (Select two)

* Run a modified IBDiagnet task as suggested by UFM Cyber AI
* Create a graph based on previous IBDiagnet results
* Create a new IBDiagnet task ✅
* Run a saved IBDiagnet task ✅

[https://docs.nvidia.com/networking/display/ufmenterpriseumv6140/ibdiagnet+tab](https://docs.nvidia.com/networking/display/ufmenterpriseumv6140/ibdiagnet+tab)

#### Question 12

You would like to clean your topology from faulty links. Which tool should you use to **detect** them?

* Managed elements menu, under "Cables"
* Network Map
* UFM Telemetry display for received packets across the fabric
* Fabric Health Reports ✅

[https://docs.nvidia.com/networking/display/ufmenterpriseumv61914/reports](https://docs.nvidia.com/networking/display/ufmenterpriseumv61914/reports)

#### Question 13

Which of the following tools provides you with historic graphical data on the different aspects of your fabric? (Select two)

* Daily Reports ✅
* Telemetry "Top X" displays
* The "Events and Alarms" menu
* Telemetry "Timeseries" displays ✅
* The "Inventory" Display



#### Question 14

Which types of network elements can have their firmware upgraded using UFM? (Select two)

* InfiniBand Cables (Copper or Optical)
* Internally Managed Switches
* Externally Managed Switches ✅
* Host Channel Adapters ✅

<details>

<summary>Explanation</summary>

UFM (Unified Fabric Manager) primarily upgrades firmware for [**Mellanox/NVIDIA network devices**](https://www.google.com/search?q=Mellanox%2FNVIDIA+network+devices\&sca_esv=53adf50e10334de7\&rlz=1C5CHFA_enMY1068MY1068\&sxsrf=ANbL-n71bx1h9PfySEcfL7jm2xjytKGmoQ%3A1768758643112\&ei=cx1tacG9Btbn2roP5bXw4QY\&ved=2ahUKEwjLzOfT05WSAxVChlYBHV_JC7kQgK4QegQIARAB\&uact=5\&oq=Which+types+of+network+elements+can+have+their+firmware+upgraded+using+UFM%3F+\&gs_lp=Egxnd3Mtd2l6LXNlcnAiTFdoaWNoIHR5cGVzIG9mIG5ldHdvcmsgZWxlbWVudHMgY2FuIGhhdmUgdGhlaXIgZmlybXdhcmUgdXBncmFkZWQgdXNpbmcgVUZNPyAyBBAjGCdInwlQAFigB3AAeACQAQCYAVygAd4HqgECMTK4AQPIAQD4AQGYAgKgArsBmAMAkgcBMqAHjkSyBwEyuAe7AcIHBTAuMS4xyAcFgAgA\&sclient=gws-wiz-serp) like [**externally managed switches**](https://www.google.com/search?q=externally+managed+switches\&sca_esv=53adf50e10334de7\&rlz=1C5CHFA_enMY1068MY1068\&sxsrf=ANbL-n71bx1h9PfySEcfL7jm2xjytKGmoQ%3A1768758643112\&ei=cx1tacG9Btbn2roP5bXw4QY\&ved=2ahUKEwjLzOfT05WSAxVChlYBHV_JC7kQgK4QegQIARAD\&uact=5\&oq=Which+types+of+network+elements+can+have+their+firmware+upgraded+using+UFM%3F+\&gs_lp=Egxnd3Mtd2l6LXNlcnAiTFdoaWNoIHR5cGVzIG9mIG5ldHdvcmsgZWxlbWVudHMgY2FuIGhhdmUgdGhlaXIgZmlybXdhcmUgdXBncmFkZWQgdXNpbmcgVUZNPyAyBBAjGCdInwlQAFigB3AAeACQAQCYAVygAd4HqgECMTK4AQPIAQD4AQGYAgKgArsBmAMAkgcBMqAHjkSyBwEyuAe7AcIHBTAuMS4xyAcFgAgA\&sclient=gws-wiz-serp) and [**Host Channel Adapters (HCAs)**](https://www.google.com/search?q=Host+Channel+Adapters+%28HCAs%29\&sca_esv=53adf50e10334de7\&rlz=1C5CHFA_enMY1068MY1068\&sxsrf=ANbL-n71bx1h9PfySEcfL7jm2xjytKGmoQ%3A1768758643112\&ei=cx1tacG9Btbn2roP5bXw4QY\&ved=2ahUKEwjLzOfT05WSAxVChlYBHV_JC7kQgK4QegQIARAE\&uact=5\&oq=Which+types+of+network+elements+can+have+their+firmware+upgraded+using+UFM%3F+\&gs_lp=Egxnd3Mtd2l6LXNlcnAiTFdoaWNoIHR5cGVzIG9mIG5ldHdvcmsgZWxlbWVudHMgY2FuIGhhdmUgdGhlaXIgZmlybXdhcmUgdXBncmFkZWQgdXNpbmcgVUZNPyAyBBAjGCdInwlQAFigB3AAeACQAQCYAVygAd4HqgECMTK4AQPIAQD4AQGYAgKgArsBmAMAkgcBMqAHjkSyBwEyuAe7AcIHBTAuMS4xyAcFgAgA\&sclient=gws-wiz-serp), using its built-in tools ([MFT](https://www.google.com/search?q=MFT\&sca_esv=53adf50e10334de7\&rlz=1C5CHFA_enMY1068MY1068\&sxsrf=ANbL-n71bx1h9PfySEcfL7jm2xjytKGmoQ%3A1768758643112\&ei=cx1tacG9Btbn2roP5bXw4QY\&ved=2ahUKEwjLzOfT05WSAxVChlYBHV_JC7kQgK4QegQIARAF\&uact=5\&oq=Which+types+of+network+elements+can+have+their+firmware+upgraded+using+UFM%3F+\&gs_lp=Egxnd3Mtd2l6LXNlcnAiTFdoaWNoIHR5cGVzIG9mIG5ldHdvcmsgZWxlbWVudHMgY2FuIGhhdmUgdGhlaXIgZmlybXdhcmUgdXBncmFkZWQgdXNpbmcgVUZNPyAyBBAjGCdInwlQAFigB3AAeACQAQCYAVygAd4HqgECMTK4AQPIAQD4AQGYAgKgArsBmAMAkgcBMqAHjkSyBwEyuAe7AcIHBTAuMS4xyAcFgAgA\&sclient=gws-wiz-serp) and [flint](https://www.google.com/search?q=flint\&sca_esv=53adf50e10334de7\&rlz=1C5CHFA_enMY1068MY1068\&sxsrf=ANbL-n71bx1h9PfySEcfL7jm2xjytKGmoQ%3A1768758643112\&ei=cx1tacG9Btbn2roP5bXw4QY\&ved=2ahUKEwjLzOfT05WSAxVChlYBHV_JC7kQgK4QegQIARAG\&uact=5\&oq=Which+types+of+network+elements+can+have+their+firmware+upgraded+using+UFM%3F+\&gs_lp=Egxnd3Mtd2l6LXNlcnAiTFdoaWNoIHR5cGVzIG9mIG5ldHdvcmsgZWxlbWVudHMgY2FuIGhhdmUgdGhlaXIgZmlybXdhcmUgdXBncmFkZWQgdXNpbmcgVUZNPyAyBBAjGCdInwlQAFigB3AAeACQAQCYAVygAd4HqgECMTK4AQPIAQD4AQGYAgKgArsBmAMAkgcBMqAHjkSyBwEyuAe7AcIHBTAuMS4xyAcFgAgA\&sclient=gws-wiz-serp)) for in-band updates, and can also manage firmware for [**UFM appliances themselves**](https://www.google.com/search?q=UFM+appliances+themselves\&sca_esv=53adf50e10334de7\&rlz=1C5CHFA_enMY1068MY1068\&sxsrf=ANbL-n71bx1h9PfySEcfL7jm2xjytKGmoQ%3A1768758643112\&ei=cx1tacG9Btbn2roP5bXw4QY\&ved=2ahUKEwjLzOfT05WSAxVChlYBHV_JC7kQgK4QegQIARAH\&uact=5\&oq=Which+types+of+network+elements+can+have+their+firmware+upgraded+using+UFM%3F+\&gs_lp=Egxnd3Mtd2l6LXNlcnAiTFdoaWNoIHR5cGVzIG9mIG5ldHdvcmsgZWxlbWVudHMgY2FuIGhhdmUgdGhlaXIgZmlybXdhcmUgdXBncmFkZWQgdXNpbmcgVUZNPyAyBBAjGCdInwlQAFigB3AAeACQAQCYAVygAd4HqgECMTK4AQPIAQD4AQGYAgKgArsBmAMAkgcBMqAHjkSyBwEyuAe7AcIHBTAuMS4xyAcFgAgA\&sclient=gws-wiz-serp), including various plugins, by utilizing the UFM server's software and sometimes direct USB/CLI methods.&#x20;

**Network Elements & Devices:**

* **Switches:** UFM supports in-band firmware upgrades for externally managed Mellanox/NVIDIA switches.
* [**Host Channel Adapters (HCAs)**](https://www.google.com/search?q=Host+Channel+Adapters+%28HCAs%29\&sca_esv=53adf50e10334de7\&rlz=1C5CHFA_enMY1068MY1068\&sxsrf=ANbL-n71bx1h9PfySEcfL7jm2xjytKGmoQ%3A1768758643112\&ei=cx1tacG9Btbn2roP5bXw4QY\&ved=2ahUKEwjLzOfT05WSAxVChlYBHV_JC7kQgK4QegQIAxAC\&uact=5\&oq=Which+types+of+network+elements+can+have+their+firmware+upgraded+using+UFM%3F+\&gs_lp=Egxnd3Mtd2l6LXNlcnAiTFdoaWNoIHR5cGVzIG9mIG5ldHdvcmsgZWxlbWVudHMgY2FuIGhhdmUgdGhlaXIgZmlybXdhcmUgdXBncmFkZWQgdXNpbmcgVUZNPyAyBBAjGCdInwlQAFigB3AAeACQAQCYAVygAd4HqgECMTK4AQPIAQD4AQGYAgKgArsBmAMAkgcBMqAHjkSyBwEyuAe7AcIHBTAuMS4xyAcFgAgA\&sclient=gws-wiz-serp)**:** Similar to switches, HCAs can also receive in-band firmware updates managed by UFM.
* [**Cable Transceivers**](https://www.google.com/search?q=Cable+Transceivers\&sca_esv=53adf50e10334de7\&rlz=1C5CHFA_enMY1068MY1068\&sxsrf=ANbL-n71bx1h9PfySEcfL7jm2xjytKGmoQ%3A1768758643112\&ei=cx1tacG9Btbn2roP5bXw4QY\&ved=2ahUKEwjLzOfT05WSAxVChlYBHV_JC7kQgK4QegQIAxAE\&uact=5\&oq=Which+types+of+network+elements+can+have+their+firmware+upgraded+using+UFM%3F+\&gs_lp=Egxnd3Mtd2l6LXNlcnAiTFdoaWNoIHR5cGVzIG9mIG5ldHdvcmsgZWxlbWVudHMgY2FuIGhhdmUgdGhlaXIgZmlybXdhcmUgdXBncmFkZWQgdXNpbmcgVUZNPyAyBBAjGCdInwlQAFigB3AAeACQAQCYAVygAd4HqgECMTK4AQPIAQD4AQGYAgKgArsBmAMAkgcBMqAHjkSyBwEyuAe7AcIHBTAuMS4xyAcFgAgA\&sclient=gws-wiz-serp)**:** UFM can also perform firmware updates (burns) for second-source cable transceivers.&#x20;

**UFM Software & Appliance Components:**

* [**UFM Enterprise/Appliance**](https://www.google.com/search?q=UFM+Enterprise%2FAppliance\&sca_esv=53adf50e10334de7\&rlz=1C5CHFA_enMY1068MY1068\&sxsrf=ANbL-n71bx1h9PfySEcfL7jm2xjytKGmoQ%3A1768758643112\&ei=cx1tacG9Btbn2roP5bXw4QY\&ved=2ahUKEwjLzOfT05WSAxVChlYBHV_JC7kQgK4QegQIBRAB\&uact=5\&oq=Which+types+of+network+elements+can+have+their+firmware+upgraded+using+UFM%3F+\&gs_lp=Egxnd3Mtd2l6LXNlcnAiTFdoaWNoIHR5cGVzIG9mIG5ldHdvcmsgZWxlbWVudHMgY2FuIGhhdmUgdGhlaXIgZmlybXdhcmUgdXBncmFkZWQgdXNpbmcgVUZNPyAyBBAjGCdInwlQAFigB3AAeACQAQCYAVygAd4HqgECMTK4AQPIAQD4AQGYAgKgArsBmAMAkgcBMqAHjkSyBwEyuAe7AcIHBTAuMS4xyAcFgAgA\&sclient=gws-wiz-serp\&mstk=AUtExfD4QsGlx-eET4aOH4PwX9XC1T-vHfT_z2uQ8lDvITOFDVeUE7W5nW6CcBG9DRKxKjyQVL3C9K1Xz1FRLdbXHRtvsO9eZnTbwG-2wwcYBtqZpf2NFToZpPQOEUCxfB7IP6pMmS0YnmPXosda6-TxoCK80RC1hGPi8l7SguzzCejBx76wWQHglFnRwdyqiFViySBueOODiovIbo4D0-uuKNVcLG0yEIKl5yCF-t2VJZ5FhsHXdjNS2O14EYl36JurjnaxYTO2lG7flq3i8IXMV6Cu6RZIXN8BjPbA7v-NvZ4yWfb9pDCGLL0eXYITpxmJdNmrJ2P__YVpyk1TGbaH8egs2nGYu65x_wiPt9NrcYtjA75jthkWREPeNooqLOFpkSbhA-dPu-PQLrUKI1Rg3Q\&csui=3)**:** The UFM server software, operating system, and associated components (like HA, Docker containers) are upgraded through specific procedures, often involving CLI commands or appliance image upgrades.
* **UFM Plugins:** Various UFM plugins, such as the GNMI-Telemetry Plugin, rest-rdma Plugin, and others, can also be upgraded as part of the UFM software update process.&#x20;

**How it Works:**

* **In-Band Updates:** For switches and HCAs, UFM uses the Mellanox Firmware Toolkit (MFT) and the `flint` utility on the UFM server to burn firmware directly over the network, requiring no IP connectivity but needing correct PSID recognition.
* **UFM Appliance Upgrades:** These often involve running upgrade scripts on the UFM server and potentially a failover process for High Availability (HA) setups.&#x20;

</details>

#### Question 15

What is a Node Description?

* A label given to a node by the administrator ✅
* A combination of model and number assigned to the node by UFM
* A device identifier provided by the vendor
* A generic GUID given to an InfiniBand device

In lecture notes

#### Question 16

Which of the following are NOT necessary for a standalone docker installation of UFM? (Select two)

* The correct license file is installed in the license directory
* Make sure that Docker is up and running
* All servers in the fabric must run the same OS ✅
* Pacemaker, pc, and drbd-utils must be installed ✅

In lecture notes (standalone have less pre-requisites than HA setup, the other 2 are under HA)

#### Question 17

When the UFM creates a new tenant in a Cloud environment, the first step taken should be:

* Request URL POST operation
* Allocate the tenant resources POST operation
* Add Port to Existing Network POST operation
* New Network creation POST operation ✅

<details>

<summary>Explanation</summary>

Based on the NVIDIA UFM (Unified Fabric Manager) documentation for cloud environments, when creating a new tenant (e.g., in an OpenStack-based cloud), the first step taken by the system, often driven by the OpenStack ML2 plugin, is to **create a new network/partition via a POST operation**. Specifically, the process involves the following initial steps:

1. **Create a new network** via a POST operation.
2. **Add a port** to the existing network.
3. **Assign PKeys (Partition Keys)** to isolate the tenant.&#x20;

This process ensures that bare metal resources are reserved and isolated for the new tenant within the InfiniBand fabric.&#x20;

</details>



#### Question 18

UFM detected a “Bad M\_Key” event. Which of the following is the most likely cause?

* One of the tenant's nodes went down
* A tenant has attempted to get data from another tenant's node by sending a Nodeinfo MAD ✅
* A tenant attempted to control the fabric by running a subnet manager on a tenant node
* One tenant has attempted to send traffic to a different tenant's node

<details>

<summary>Answer</summary>

A "Bad M\_Key" (Management Key) event in UFM indicates that a component in the InfiniBand fabric (typically an HCA or switch) received a management packet (MAD) with an incorrect or unauthorized M\_Key, leading to the packet being dropped. The most likely causes are:

* **Subnet Manager (SM) Re-election/Re-start:** If a new SM takes over and starts pushing a new M\_Key, or if a switch is not synchronized with the current master SM's M\_Key, a mismatch occurs.
* **M\_Key Configuration Mismatch:** A mismatch in the `gv.cfg` (UFM configuration) or OpenSM configuration settings (e.g., `m_key` or `m_key_per_port` settings) between the UFM server and the switches/nodes.
* **Security Violation (Attempted Unauthorized Access):** A node or unauthorized device is attempting to perform administrative actions (e.g., changing port configurations) without the correct M\_Key.
* **Rebooting a node without properly handling the M\_Key:** If a node reboots, it might still have an old M\_Key set in its hardware, causing it to reject new packets from the current SM.&#x20;

**Key Recommendations to Resolve:**

* **Verify `gv.cfg`:** Ensure that the `m_key` and `m_key_per_port` parameters are consistently configured in `gv.cfg`.
* **Check `m_key_per_port`:** If `m_key_per_port` is set to `true`, consider the security implications and ensure all nodes are properly registered with the SM.
* **Restart SM:** If the issue is persistent, restarting the Subnet Manager might resolve the discrepancy.
* **Check Host Driver/Settings:** In some cases, updating the HCA driver or ensuring partition settings are correct can resolve the issue.&#x20;

</details>

#### Question 19

Which of the following files contain crucial parameters for cluster management? (Select two)

* gv.cfg ✅
* UFM.lic
* opensm.conf ✅
* opensm.log

Last unit

#### Question 20

Which of the following UFM functions allows you to set a Node Description of an externally managed switch?

* “Set Logical Server” -> Search switch name -> Click “Sent Node Description”
* Managed Elements -> Right Click on Switch -> “Set Node Description” ✅
* POST /ufmRestApi/switches/\<switch name>\&node\_desc=new\_node description
* “Manage Node Telemetry” -> Node\_name -> Click “Change value” -> enter new Node Description

(First few lectures)
