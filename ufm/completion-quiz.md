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
* All of the above ✅

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

#### Question 8

What information is listed under "Device Information" when observing a particular network component? (Select three)

* Topology snapshots associated with the device
* Suggested actions regarding device alarms
* Events and alarms detected on the device ✅
* Device Ports (Physical and Virtual) ✅
* Linked Cables attached to the device's ports and their details ✅

#### Question 9

Which of the following are types of logs that may be displayed in “UFM Logs” (under “System Health”)? (Select three)

* SM Logs ✅
* UFM Logs ✅
* Switch OS Logs
* ibdiagnet Logs ✅
* Event Logs

#### Question 10

Why would you visit the “UFM Health” tab (under the “System Health” Menu)?

* To determine whether UFM’s functionalities are working properly
* To collate data recorded in the UFM Logs related to alarms or warnings
* To track changes made to the UFM processes, a system error event
* All of the above ✅

#### Question 11

Which of the following operations can be performed in the "IBDiagnet" tab under the "System Health" menu? (Select two)

* Run a modified IBDiagnet task as suggested by UFM Cyber AI
* Create a graph based on previous IBDiagnet results
* Create a new IBDiagnet task ✅
* Run a saved IBDiagnet task ✅

#### Question 12

You would like to clean your topology from faulty links. Which tool should you use to detect them?

* Managed elements menu, under "Cables"
* Network Map
* UFM Telemetry display for received packets across the fabric
* Fabric Health Reports ✅

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

#### Question 15

What is a Node Description?

* A label given to a node by the administrator ✅
* A combination of model and number assigned to the node by UFM
* A device identifier provided by the vendor
* A generic GUID given to an InfiniBand device

#### Question 16

Which of the following are NOT necessary for a standalone docker installation of UFM? (Select two)

* The correct license file is installed in the license directory
* Make sure that Docker is up and running
* All servers in the fabric must run the same OS ✅
* Pacemaker, pc, and drbd-utils must be installed ✅

#### Question 17

When the UFM creates a new tenant in a Cloud environment, the first step taken should be:

* Request URL POST operation
* Allocate the tenant resources POST operation
* Add Port to Existing Network POST operation
* New Network creation POST operation ✅

#### Question 18

UFM detected a “Bad M\_Key” event. Which of the following is the most likely cause?

* One of the tenant's nodes went down
* A tenant has attempted to get data from another tenant's node by sending a Nodeinfo MAD ✅
* A tenant attempted to control the fabric by running a subnet manager on a tenant node
* One tenant has attempted to send traffic to a different tenant's node

#### Question 19

Which of the following files contain crucial parameters for cluster management? (Select two)

* gv.cfg ✅
* UFM.lic
* opensm.conf ✅
* opensm.log

#### Question 20

Which of the following UFM functions allows you to set a Node Description of an externally managed switch?

* “Set Logical Server” -> Search switch name -> Click “Sent Node Description”
* Managed Elements -> Right Click on Switch -> “Set Node Description” ✅
* POST /ufmRestApi/switches/\<switch name>\&node\_desc=new\_node description
* “Manage Node Telemetry” -> Node\_name -> Click “Change value” -> enter new Node Description
