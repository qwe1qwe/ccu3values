# ccu3values
Reads operating data from a CCU with XMLRPC plugin and makes them available for further processing.

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes..

### Prerequisites
  * Python 3.x

### Installing 

#### Debian based 
```
sudo apt-get update 
sudo apt-get -y upgrade
apt-get install python3 python-pip python-dev
cd your_project_folder
git clone https://github.com/StowasserH/ccu3values.git
bash install.sh
```

### Configuration Zabbix

Install [XML-API](https://github.com/homematic-community/XML-API) on your CCU.
After reboot a token can be obtained by tokenregister.cgi.

Import the yaml or xml file from "zabbix" folder as template in Zabbix-UI.

Add CCU as host in Zabbix and add following macros (example values) and use ccu_values template:

|Macro|Value|
|-|-|
|{$CCU_CACHE_USE}|--cache-use|
|{$CCU_CACHE_FILE}|/tmp/ccu.cache|
|{$CCU_CACHE_TIME}|60|
|{$CCU_XMLRPC}|http://ccu3-webui/addons/xmlapi/|
|{$CCU_TOKEN}|aaBBccDDeeFFggHH|
|{$CCU_HTTPCHECK}|http://ccu3-webui/login.htm|

## Development

Feel free to use and modify it, but please help me to improve it.

### Coding style

If you commit code pls try to format it in [PEP8](https://www.python.org/dev/peps/pep-0008/)


## Authors

* **Harald Stowasser** - *Initial work* - [StowasserH](https://github.com/StowasserH)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
