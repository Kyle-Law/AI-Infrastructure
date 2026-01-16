# Managed Elements each window

This comprehensive guide covers the Managed Elements section of the NVIDIA UFM Web UI. This area is the "Command Center" for the physical and virtual assets of your InfiniBand fabric.

***

### 1. Devices Window

The primary inventory for all hardware (Switches, HCAs, Gateways).

* Key Columns: Health status (color-coded by alarm severity), Device Name, Type, GUID, and Firmware version.
* Critical Actions (Right-Click):
  * Isolate: Logically removes the device from the fabric traffic while keeping it visible for management.
  * No Discover: Forces the Subnet Manager to ignore the device entirely.
  * Firmware Upgrade: Triggers in-band or agent-based firmware burning.
  * System Dump: Collects a diagnostic log specifically for that hardware unit.
* Deep Dive: Clicking a device opens a detailed view with tabs for Ports, Cables, and Events specific to that unit.

### 2. Ports Window

Provides a granular view of every physical port in the fabric.

* Key Columns: Port Name/Number, State (Active/Down), Width (e.g., 4x), Speed (e.g., NDR), and Peer Information.
* Troubleshooting Features:
  * Filtering: Quickly view only "Active" or only "Down" ports.
  * Physical Grade/Eye Info: Shows signal quality (Eye Opening) data, which is vital for identifying physical layer degradation before a link fails.
  * Persistence: Enable/Disable actions on ports are persistent through switch reboots.

### 3. Virtual Ports Window

Specific to virtualized environments (e.g., SR-IOV).

* Function: Maps virtual port GUIDs to the physical HCAs and switches hosting them.
* Visibility: Only appears if virtualization is enabled in the UFM configuration (`gv.cfg`).
* Navigation: Allows you to right-click a virtual port and "Go to Physical Port" to trace traffic back to actual hardware.

### 4. Unhealthy Ports Window

A focused "hit list" for maintenance teams.

* Logic: Automatically pulls any port experiencing errors, High Bit Error Rates (BER), or unexpected "Down" states.
* Auto-Isolation: If the High-BER auto-isolation feature is on, ports that fail thresholds appear here automatically for review.

### 5. Cables Window

Inventory management for all optical and copper interconnects.

* Data Points: Manufacturer, Part Number, Serial Number, and Revision.
* Diagnostics: Shows temperature and power levels for transceivers.
* Mapping: Displays the "Source" and "Destination" ports for every cable, acting as a digital "cabling map."

### 6. Groups Window

Administrative tool for bulk management.

* Creation: Group devices by rack, function (Storage/Compute), or tier (Spine/Leaf).
* Bulk Firmware Upgrade: Instead of updating 100 servers individually, you right-click the "Compute Group" and initiate a mass burn.
* Health Summary: Shows the aggregated health state of the group members.

### 7. Inventory Window

The "Asset Manager" view.

* Function: Provides a roll-up of all FRUs (Field Replaceable Units).
* Components: Lists Fans, Power Supplies, and ASICs.
* Environmental Tracking: You can expand the Fan item to see real-time RPMs and the Power Supply item to check electrical health.

### 8. HCAs Window

Dedicated view for Host Channel Adapters (the "network cards" in your servers).

* Details: Displays OFED version, host IP addresses, and HCA-specific GUIDs.
* Management: Simplifies tracking which servers have outdated drivers or firmware compared to the rest of the cluster.

***

#### Comparison of Managed Elements

| **Window** | **Best For...** | **Primary Action**                |
| ---------- | --------------- | --------------------------------- |
| Devices    | General Admin   | Isolate/Discover nodes            |
| Ports      | Performance     | Check Link Speed & Error Counters |
| Cables     | Physical Repair | Locate specific Serial Numbers    |
| Groups     | Maintenance     | Bulk Firmware Upgrades            |
| Inventory  | Facilities/Ops  | Monitor PSU & Fan speeds          |
