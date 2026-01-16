# Refined

## Unit 3.1: Monitoring Fabric Health and Event Management

To effectively manage an InfiniBand fabric, UFM transforms raw telemetry into actionable insights through three primary mechanisms: Alarms, Logs, and Reports.

***

### 1. Events and Activities

UFM tracks over 400+ predefined event types. Understanding how to filter and react to these is the core of fabric monitoring.

#### Event Categories (Severities)

Events are classified into four severity levels:

1. Info: Routine operational updates.
2. Warning: Potential issues that don't yet impact traffic.
3. Minor: Non-critical failures or degradations.
4. Critical: Immediate threats to fabric stability or performance.

#### Customizing Event Policies

The Event Policies tab allows you to tailor UFM to your specific data center requirements:

* Severity Modification: Override the default severity of any of the 400+ events.
* Logging Destinations: Choose per-event whether to send data to Syslog, a local Log File, or SNMP traps for 3rd-party management clients.
* UI Visibility (TTL): Define the Time-to-Live (TTL) for how long an alarm remains visible on the Web UI dashboard.

#### Dashboard Visibility

* Top 5 Lists: The main dashboard provides instant visibility into the Top 5 Alarmed Switches, helping prioritize hardware replacement.
* Recent Activities: A sidebar on the right of the UI displays a live feed of events, which can be filtered by severity for quick audits.

***

### 2. System Health Menu

This menu is the "Command Center" for deep-dive diagnostics and historical data. It is divided into several specialized tabs:

#### UFM & Fabric Health

* UFM Health: Monitors the status of the UFM server itself (CPU, Memory, Service status).
* Fabric Health Tab: Allows you to run On-Demand Tests. You can trigger a suite of diagnostic tests and have the results automatically emailed to a predefined list of recipients.
* Fabric Validation: A summary report checking for configuration errors, such as mismatched link speeds or MTU settings across the fabric.

#### Logging and Snapshots

* UFM Logs: Centralized repository for Event logs and Subnet Manager (SM) logs.
  * _Features:_ Filter by time range, limit entry counts, and full-text search.
* UFM Snapshot: Creates a "point-in-time" backup of the UFM Database and configuration files.
  * _Troubleshooting:_ You can include specific debug info in the snapshot to send to NVIDIA support.

***

### 3. Topology Management and Advanced Tools

Maintaining the "Golden Standard" of your network layout.

#### Topology Compare

This tool ensures the physical cabling matches the intended design.

* Master Topology: The "known good" baseline of the fabric.
* Comparison Engine: Run periodic or manual comparisons between the Current Topology and the Master Topology.
* Updates: If a change was intentional (e.g., adding a new rack), you can "Update Master Topology" to set the new baseline.

#### IBDiagnet (InfiniBand Diagnostics)

* Integrates the standard `ibdiagnet` tool into the GUI.
* Users can click "New" to create a manual diagnostic run or Schedule it to run automatically (e.g., every midnight) to catch intermittent cable drops or symbol errors.

#### Daily Reports

* Concentrated summaries of fabric performance and health sent to administrators, reducing the need to manually check the UI daily.
