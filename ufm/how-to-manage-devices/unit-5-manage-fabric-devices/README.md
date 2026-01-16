# Unit 5 - Manage Fabric Devices

Documentation: [https://docs.nvidia.com/networking/display/ufmenterpriseumv6201/managed+elements](https://docs.nvidia.com/networking/display/ufmenterpriseumv6201/managed+elements)

Follow the official docs for in-depth understanding





objectives

display device params info

detail  device and ports operational status

display alarm and event indications

display switch and HCA firmware upgrade



Summary

Display device port params

configure device names

firmware upgrade process using groups :white\_check\_mark: - mlxfwreset to reboot and apply updated

Filter devices with alarm levels :white\_check\_mark:

Isolating devices (for maintenance)



manage&#x20;

keep constant trac...

keep up to date of other immport param

firmware version and more

take actions such as burning firmware..

while being provide graphic report



fabric device with ufm



menu on the left

enable deep dive&#x20;



Managed Elements



device submenu tasks



General - ports alarms events hcas device acccess vertual networkng

ports provde addictional info like severity, port name, peer node

easy to learn that port like... 6/1 -> mtlac09



show which alarms affected that device



cables tab - serial, source, destination port

Virtual NEtworking tab - physical ports



filtering menu like severity, name, guid, type...

fien tuning sesarch features - multiple search criteria



isolating a device

devices - right click a device - mark as unhealthy - Isolate (remain visible on topology but no network)

No Discover - makes the device disappear from the  toplogy



Groups tab

ufm allows admin to create a group of nodes

easier collection of the group - simultaneous firmware update

+New icon group > name > type > Description > select desired servers



Upgrade group firmware

right click -> Firmware upgrade -> In Band

Job starts running - with job summary page

run mlxfwreset to reboot devices to new firmware



Ports

easy search-  MTU, severity, name,&#x20;



Virtual Ports

in many clusters deployed - many machine are virtual

status, system name, port, virtual port GUID, virutal Port LID





