Takze, měl jsem docela hodně problemu během instalace pfSence a Zabbix Appliance. Konečně jsem je nastavil na NAT + intnet tak, aby se mohli pingovat navzajem(192.168.1.1, 192.168.1.10)
![PING](./Images/ping.jpg) 
![ips](./Images/ips.jpg)

udělal jsem portforvarding 
![porf](./Images/portforw.jpg)

ale pfSense pořad děla nejake blbosti, nechce se otevirat Web GUI i když je nastaven spravně, přestal se spouštět prez vagrant up atd.


Po 20-30 minut oprav - pfsense web gui stale nefunguje.
/*Na 3kolnim po4ita4i funguje, i kdyz postup byl UPLNĚ stejny.

Nastavil jsem pravidlo SNMP na pfSense WEB GUI
![snmppf](./Images/snmppf.png)

zkusil jsem prikazy 

sudo dnf install net-snmp-utils -y
snmpwalk -v2c -c public 192.168.1.1 system
![snmp](./Images/snmp.png)
