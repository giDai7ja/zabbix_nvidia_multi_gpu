This template is for Zabbix to monitor multiple Nvidia GPUs

For nvidia GPU monitoring, zabbix offers a standard [template](https://github.com/zabbix/community-templates/tree/main/Server_Hardware/Other/template_nvidia-smi_integration). The disadvantage is that it only allows monitoring one GPU
Of course there are other templates, but this one has some advantages
For example, this template uses only one user parameter and does not require additional scripts

## Features

* Low-level discovery of all the graphics Nvidia cards
* Prototype items and triggers for the most important parameters
* General status panel

## Installation

* Upload the nvidia_gpus.conf user settings file to the directory according to your agent settings. [More...](https://www.zabbix.com/documentation/current/en/manual/appendix/config/zabbix_agentd#include)
* Restart the azbbix-agent
* Import template zbx_Nvidia_GPUs.json and link this template to the monitored host


This template is set up and tested on a server with nine Nvidia graphics cards
Comments, suggestions and help to improve this template are welcome
