# NVidia MultiGPU

## Overview

This template is for Zabbix to monitor multiple NVidia GPUs

For nvidia GPU monitoring, zabbix offers a standard [template](https://github.com/zabbix/community-templates/tree/main/Server_Hardware/Other/template_nvidia-smi_integration). The disadvantage is that it only allows monitoring one GPU. Of course there are other templates, but this one has some advantages. For example, this template uses only one user parameter and does not require additional scripts

### Features

* Low-level discovery of all the graphics Nvidia cards
* Prototype items and triggers for the most important parameters
* General status panel

### Installation

* Upload the nvidia_gpus.conf user settings file to the directory according to your agent settings
* Restart the zabbix-agent
* Import template zbx_nvidia_multigpu.yaml and link this template to the monitored host

This template is set up and tested on a server with nine Nvidia graphics cards. Comments, suggestions and help to improve this template are welcome

## Macros used

There are no macros links in this template.

## Template links

There are no template links in this template.

## Discovery rules

|Name|Description|Type|Key and additional info|
|----|-----------|----|----|
|GPU Data|<p>Data collection by GPUs</p>|`SNMP agent`|gpu.data<p>Update: 1m</p>|

## Items collected

Common Items
|Name|Description|Type|Key and additional info|
|----|-----------|----|----|
|GPU Count|<p>Number of GPUs detected</p>|`Dependent items`|gpu.count<p>Update: 1m</p>|
|GPU Driver Version|<p>GPU driver version</p>|`Dependent items`|gpu.driver_version<p>Update: 1m</p>|
|GPU Power Total|<p>Power consumption of all GPUs</p>|`Calculated items`|gpu.power_total<p>Update: 1m</p>|
|GPUs Maximum Temperature|<p>Temperature of the hottest GPU</p>|`Calculated items`|gpu.temp_max<p>Update: 1m</p>|
|GPU Utilization Total|<p>Total GPU utilisation</p>|`Calculated items`|gpu.utilization_total<p>Update: 1m</p>|


Items for each GPU found
|Name|Description|Type|Key and additional info|
|----|-----------|----|----|
|GPU Power|<p>-</p>|`Zabbix agent`|gpu.power<p>Update: 1m</p>|
|GPU Free Memory|<p>-</p>|`Zabbix agent`|gpu.mfree<p>Update: 1m</p>|
|GPU Utilisation|<p>-</p>|`Zabbix agent`|gpu.utilization<p>Update: 1m</p>|
|GPU Total Memory|<p>-</p>|`Zabbix agent`|gpu.mtotal<p>Update: 1m</p>|
|GPU Temperature|<p>-</p>|`Zabbix agent`|gpu.temperature<p>Update: 1m</p>|
|GPU Used Memory|<p>-</p>|`Zabbix agent`|gpu.used<p>Update: 1m</p>|
|GPU Fan Speed|<p>-</p>|`Zabbix agent`|gpu.fanspeed<p>Update: 1m</p>|


## Triggers

There are no triggers in this template.

## Author

Vladimir Eliseev
