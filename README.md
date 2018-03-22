# WarBerryPi 
![alt tag](https://github.com/secgroundzero/warberry/blob/master/Warberry_Logo_Transparent.png)

[![ToolsWatch Best Tools](https://www.toolswatch.org/badges/toptools/2016.svg)](https://www.toolswatch.org/2017/02/2016-top-security-tools-as-voted-by-toolswatch-org-readers/)
[![Black Hat Arsenal](https://www.toolswatch.org/badges/arsenal/2016.svg)](https://www.blackhat.com/us-16/arsenal.html)
![GPLv3 License](https://img.shields.io/badge/License-GPLv3-red.svg)
[![Python 2.6|2.7](https://img.shields.io/badge/python-2.6|2.7-yellow.svg)](https://www.python.org/)
[![Twitter](https://img.shields.io/badge/twitter-@sec_groundzero-blue.svg)](https://twitter.com/sec_groundzero)


**WarBerryPi** was built to be used as a hardware implant during red teaming scenarios where we want to obtain as much information 
as possible in a short period of time with being as stealth as possible. 
Just find a network port and plug it in. The scripts have been designed in a way that the approach is targeted to avoid noise 
in the network that could lead to detection and to be as efficient as possible. 
The WarBerry script is a collection of scanning tools put together to provide that functionality.



#### Disclaimer
This tool is only for academic purposes and testing  under controlled environments. Do not use without obtaining proper authorization
from the network owner of the network under testing.
The author bears no responsibility for any misuse of the tool.


#### Usage

To get a list of all options and switches use:

```python warberry.py -h```

```

Options:

  --version                             show program's version number and exit
  -h, --help                            show this help message and exit
  -p PACKETS, --packets=PACKETS         Number of Network Packets to capture
  -I IFACE, --interface=IFACE           Network Interface to use. Default: eth0
  -N NAME, --name=NAME                  Hostname to use. Default: Auto
  -i INTENSITY, --intensity=INTENSITY   Port scan intensity. Default: T4
  -Q, --quick                           Scan using threats. Default: Off
  -P, --poison                          Turn Poisoning on/off. Default: On
  -H, --hostname                        Do not Change WarBerry hostname Default: Off
  -e, --enumeration                     Disable Enumeration mode. Default: Off
  -M, --malicious                       Enable Malicious only mode. Default: Off
  -B, --bluetooth                       Enable Bluetooth scanning. Default: Off
  -r, --recon                           Enable Recon only mode. Default: Off
  -W, --wifi                            Enable WiFi scanning. Default: Off
  -S, --sniffer                         Enable Sniffer only mode. Default: Off
  -C, --clear                           Clear previous output folders in ../Results
  -m, --man                             Print WarBerry man pages


example usage: sudo python warberry.py -a -T                Attack all TCP Ports
               sudo python warberry.py -r                   Use only the recon modules
               sudo python warberry.py -H -I wlan0          Use the wlan0 interface and dont change hostname
               sudo python warberry.py -I eth0 -i -T3       Use the eth0 interface and T3 scanning intensity
               sudo python warberry.py -I eth0 -N HackerPC  Use the eth0 interface and change hostname to HackerPC

```



### Installation

Run ```sudo bash setup.sh```



### Reporting 

Download the **/RESULTS** folder into /var/www, /Library/Webserver/Documents/  or XAMPP web directory depending on your OS and setup.

Download the warberry.db file locally and save it into **Reporting/** .

Change file Config.php under Reporting/WarberryReporting/SQLiteConnection/php to use the correct path of warberry.db

Run index.html under **Reporting/**
