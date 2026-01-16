# Unit 5.2 - UFM Firmware Upgrade

Firmware upgrade on network devices



HCA / Externally managed switches

individaully / parallel / using groups of selected nodes



Prerequisites:

1. Get file from developer.nvidia.com
2. copy to Firmware repo main ufm directory: /opt/ufm/files/userdata/fw



Steps;

1. Managed elements tab
2. SSH to specific server&#x20;

```
ibstate -d mlx5_0 ## display current firmware version
mlxfwreset -d mlx5_0 --level 3 ## restart and apply updated version
```



Firmware Reset for Externally Managed Switches

1. right click switch to reset
2. (then the right step is empty after clicking, no next video showed up)





