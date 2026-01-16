# Refined

Analyzing congestion in a high-performance InfiniBand fabric requires moving from high-level monitoring to surgical root-cause analysis. NVIDIA UFM provides a multi-layered toolkit to identify where bottlenecks occur and why they exist.

***

### 1. Visualizing Congestion (The "Where")

#### Dashboard: Traffic Map

The Traffic Map is your first line of defense. It provides a real-time, high-level overview of fabric health.

* Dynamic Updates: The map updates automatically (typically every 30 seconds) to reflect traffic shifts.
* Congestion Bandwidth (CBW): Look for red bars, which represent normalized congestion. If you see red bars in the middle tiers (Spine switches), it often indicates a routing efficiency problem.
* Top X Lists: Use the Top 5 Congested Servers and Top 5 Congested Switches panels to immediately identify "hotspots" (e.g., `LEAF_05`, Port 12).

#### Network Map: Link Analysis

For a deep dive into physical bottlenecks, use the Link Analysis tool within the Network Map.

* Hotspot View: Select View > Link Analysis and add the Port TX Data Rate counter.
* Thresholding: Set color thresholds (e.g., Orange for >70%, Red for >90%). This allows you to trace the exact physical path of congestion, such as `Spine-02` → `Leaf-06` → `Host-07`.

***

### 2. Root Cause Analysis (The "Why")

Once you've located the congestion, use the System Health tools to determine the cause.

#### System Health: Fabric Health Tab

Run a Fabric Health Report to cross-reference congestion with hardware status.

* UFM Alarms: Check if a "faulty link" alarm exists for the congested path. A link running at a lower speed (e.g., EDR instead of HDR) due to a bad cable will cause immediate back-pressure.
* Routing Check: If hardware is healthy but congestion is high, the report might flag non-optimal routing paths.

#### Identifying Traffic Patterns

Congestion is often caused by the application's communication logic rather than hardware failure:

* Many-to-One: Many nodes sending data to a single storage node or "aggregator" simultaneously.
* Noisy Neighbors: One tenant or job consuming all available bandwidth on shared uplinks.
* Solution: Consider enabling Adaptive Routing (AR) or Congestion Control (CC) in the Subnet Manager (SM) settings to dynamically re-route traffic around these bottlenecks.

***

### 3. Future Tracking: Port Groups

To prevent recurring issues, organize your monitoring using Port Groups.

* Defining Groups: Go to Groups > New > Type: Port. You can group ports by their function (e.g., "Storage Uplinks" or "Compute Rack 1").
* Observation: The Traffic Map can be filtered by these groups. This allows you to see if congestion is specific to your storage subsystem or your compute cluster, making it easier to adjust application traffic patterns.

***

### Summary Checklist

| **Step**    | **Tool**                      | **Goal**                                                                  |
| ----------- | ----------------------------- | ------------------------------------------------------------------------- |
| 1. Detect   | Dashboard Traffic Map         | Identify if the fabric has red "Congestion" bars.                         |
| 2. Locate   | Network Map (Link Analysis)   | Pinpoint the specific switches and ports lighting up.                     |
| 3. Diagnose | Fabric Health Report          | Rule out hardware failures (Bad cables/BER errors).                       |
| 4. Mitigate | Subnet Manager / App Settings | Enable Adaptive Routing or adjust app communication.                      |
| 5. Monitor  | Port Groups                   | Create a dedicated view for the problematic ports for long-term tracking. |

#### Relevant Resources

* [UFM Fabric Dashboard Guide](https://docs.nvidia.com/networking/display/ufmenterpriseumv62311/fabric-dashboard): Detailed breakdown of the Traffic Map and Top X panels.
* [Configuring Adaptive Routing & SHIELD](https://enterprise-support.nvidia.com/s/article/How-To-Configure-Adaptive-Routing-and-SHIELD): Technical guide on how to solve congestion through routing.
* [UFM System Health & Reports](https://docs.nvidia.com/networking/display/ufmenterpriseumv6171/system-health.pdf): How to generate and interpret Fabric Health reports.
