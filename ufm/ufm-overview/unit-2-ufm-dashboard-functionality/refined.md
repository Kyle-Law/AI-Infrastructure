# Refined

### NVIDIA UFM Dashboard Overview

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The UFM Dashboard provides a real-time, centralized view of the InfiniBand fabric health, performance, and inventory. It is designed to help administrators "trace the state" of the fabric instantly.

####

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### 1. Fabric Traffic Map (Congestion Tracing)

The dashboard visualizes traffic patterns and bandwidth utilization across the network.

* Four-Tier Visualization: Traffic is typically analyzed in four logical steps:
  1. Server $$ $\rightarrow$ $$ Leaf Switch: Data leaving the hosts.
  2. Leaf Switch $$ $\rightarrow$ $$ Spine Switch: Data moving up the fabric hierarchy.
  3. Spine Switch $$ $\rightarrow$ $$ Leaf Switch: Data moving back down toward destinations.
  4. Leaf Switch $$ $\rightarrow$ $$ Server: Data reaching the target endpoint.
* Heatmaps & Color Coding: High-traffic areas and congestion points are highlighted using colors (e.g., Red for high congestion, Green for healthy flow).
* Port Diagnostics: You can drill down into specific ports to identify why a particular link is "hot" or congested.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

#### 2. Inventory & Health Monitoring

UFM acts as a single source of truth for every component in the fabric.

* Inventory Display: View the status of switches, cables, and adapters.
* Status Indicators: Components display Warning or Alarm icons if hardware failures or threshold violations occur.
* Versions Tab: Quickly verify firmware and software versions across all devices to ensure consistency and compatibility.

***

#### 3. Performance Analytics (Top 5 Charts)

The dashboard features dynamic charts to identify the most active or problematic elements in the fabric.

* Top 5 Charts: Automatically displays the "Top 5" entities for specific metrics (e.g., Top 5 most congested switches or Top 5 highest bandwidth ports).
* Customizable Metrics: You can change the display metrics for each chart (e.g., switching from "Bandwidth" to "Error Rates").
* Interactive Elements: Clicking on any element within a chart allows you to "drill down" into the specific details of 그 hardware component.

***

#### 4. Recent Activities & Events

Located on the right side of the interface, this pane serves as the fabric's "black box" recorder.

* Activity Log: Displays a live feed of all recorded details, including configuration changes and system logs.
* Navigation: You can click directly on an activity to navigate to the Events and Alarms menu for deep-dive troubleshooting.

***

### Summary Table: UFM Dashboard Quick Reference

| **Feature**   | **Function**                                                 |
| ------------- | ------------------------------------------------------------ |
| Traffic Map   | Visualizes bandwidth and congestion across 4 tiers.          |
| Inventory     | Monitors hardware health and firmware versions.              |
| Top 5 Charts  | Identifies the most active/congested components at a glance. |
| Activity Pane | Real-time log of events, errors, and system changes.         |



References

[https://docs.nvidia.com/networking/display/ufmenterpriseumv6190/fabric-dashboard](https://docs.nvidia.com/networking/display/ufmenterpriseumv6190/fabric-dashboard)
