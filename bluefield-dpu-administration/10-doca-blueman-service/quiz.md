# Quiz

### DOCA BlueMan Service and Telemetry

#### Question 1

How is the DPU data available via DOCA BlueMan Service collected?

* Via a light-weight database running in the DPU server
* Via system logs
* Via the DOCA Telemetry Service (DTS) ✅
* Via Linux dump files

> Note: DOCA BlueMan acts as a frontend visualization layer. All the system health, basic information, and performance counters it displays are gathered and provided by the DOCA Telemetry Service (DTS) running in the background on the DPU.

***

#### Question 2

The following information is available in the DOCA BlueMan Service - DPU General Information page (Select 2)

* Alert of suspicious traffic
* DPU mode of operation ✅
* Number of concurrent users
* OS name and version ✅

> Note: The "General Information" (or "Info") section of BlueMan provides hardware and software metadata. This includes the OS name/kernel version, the DPU operation mode (DPU vs. NIC mode), DOCA version, and hardware serial numbers. Traffic alerts would typically be found in a security-focused service like DOCA Flow Inspector or DOCA App Shield.

***

#### Question 3

What is the main purpose of DOCA BlueMan Service?

* It’s a graphical interface for configuring BlueField DPU parameters.
* It’s a telemetry and visualization tool for a single Bluefield DPU system ✅
* It’s a monitoring tool for visibility into all BlueField DPUs running in a datacenter.
* It’s a graphical interface for developing applications to run directly in the DPU.

> Note: BlueMan is designed as a standalone web dashboard that runs locally on a specific DPU. It provides a "one-stop shop" for a human administrator to monitor the health and status of that specific unit. For data-center-wide monitoring, tools like NVIDIA NetQ or telemetry exporters to Prometheus/Grafana are used.

***

#### References & Further Reading

* [NVIDIA Docs: DOCA BlueMan Service Guide](https://docs.nvidia.com/doca/sdk/doca-blueman-service-guide/index.html)
* [NVIDIA Docs: DOCA Telemetry Service (DTS) Guide](https://www.google.com/search?q=https://docs.nvidia.com/doca/sdk/doca-telemetry-service-guide/index.html)
* [NVIDIA DOCA Services Overview](https://www.google.com/search?q=https://docs.nvidia.com/doca/sdk/doca-services-overview/index.html)
