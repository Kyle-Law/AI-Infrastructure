# Refined

## Unit 3.2: Creating Telemetry Sessions and Visual Link Analysis

UFM allows you to move beyond basic dashboards by creating User-Defined Telemetry Sessions. These sessions provide a granular look at cables, ports, and traffic congestion using highly customizable, real-time charts.

***

### 1. Setting Up a Telemetry Session

Custom sessions allow you to focus on specific segments of the fabric or specific performance metrics.

#### Creating the Session

1. Navigate to the Telemetry Tab: Click "New Telemetry View".
2. Naming: Provide a unique name for the session. Once saved, this session will appear in the top dropdown menu for easy switching.
3. Define Session Type: \* Timeseries: Best for historical trends and live line graphs.
   * Top X & Ports: Focuses on the "worst offenders" (e.g., the top 5 most congested ports).
4. Normalize Congestion/Bandwidth: Ensure you click "Normalize Congestion" to view data as a percentage of total capacity. This makes it easier to compare links of different speeds (e.g., NDR vs. HDR).

***

### 2. Using the Network Map for Visual Telemetry

The Network Map is a dynamic tool that overlays real-time telemetry data onto your physical topology.

#### Link Analysis Mode

* Activation: Open the Network Map and click on Link Analysis.
* Adding Counters: Use the "Add Counter" dropdown and click the plus (+) icon to select the metric you want to visualize (e.g., `PortXmitData` or `PortXmitWait`).
* Thresholds & Color Coding:
  * Define a threshold (e.g., $$ $> 80\%$ $$ utilization).
  * Assign a color (e.g., Red for high congestion, Green for healthy).
  * The links on the map will instantly "light up" in the chosen color if they meet the condition.

#### Inspecting and Saving Views

* Drill Down: Clicking on a specific colored link opens a detailed list showing the cable info and the specific ports involved.
* Save View: Use the "Save As" icon on the top menu to store your customized Link Analysis. This allows you to reload the same "Congestion View" or "Error View" later without re-configuring thresholds.

***

### 3. Relevant Resources & Links

* [Telemetry User-Defined Sessions (Manual)](https://docs.nvidia.com/networking/display/ufmenterpriseumv6191/telemetry+-+user-defined+sessions): Deep dive into creating the "Top X" and "Timeseries" panels.
* [Network Map & Link Analysis Guide](https://docs.nvidia.com/networking/display/ufmenterpriseumv6175/network+map): Detailed instructions on adding counters to the map and using color-coded thresholds.
* [UFM REST API - Telemetry Endpoints](https://docs.nvidia.com/nvidia-ufm-enterprise-rest-api-guide-v6-17-0.pdf): For advanced users who want to pull these "Top X" or "Timeseries" sessions into external tools programmatically.
* [Daily Reports - Normalized Traffic](https://docs.nvidia.com/networking/display/ufmenterpriseumv6158/daily+reports+tab): Explains the math behind how UFM calculates "Normalized Congestion" mentioned in your notes.
