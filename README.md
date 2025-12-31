# Zabbix Server and Agents Configuration Files
This repository contains a docker-compose.yml file to configure a Zabbix server and a zabbix_agentd.conf file to configure the agents.
## Zabbix Server Configuration
1. Clone the Repository
```git
git clone https://github.com/ysfelhamri/zabbix-monitoring-config
```
2. Navigate to the Cloned Folder
```git
cd zabbix-monitoring-config
```
3. Run the Containers
```git
docker-compose up -d
```
4. Check the Containers
```git
docker ps
```
## Zabbix Agents Configuration
1. Install the Agent
Select your system from here :
https://www.zabbix.com/download
2. Locate the zabbix_agentd.conf File
* Linux
```git
/etc/zabbix/zabbix_agentd.conf
```
* Windows
```git
C:\Program files\Zabbix Agent\zabbix_agentd.conf
```
4. Set the IP Address of the Zabbix Server in the zabbix_agentd.conf File
```git
Server=<Zabbix_Server_IP>
```
```git
ServerActive=<Zabbix_Server_IP>
```
5. Set the Agent Name in the zabbix_agentd.conf File
```git
Hostname=<Agent_Name>
```
6. Restart the Zabbix Agent Service

* Linux
```git
systemctl restart zabbix-agent
```
* Windows
```git
net stop Zabbix agent
```
```git
net start Zabbix agent
```
## Connecting the Zabbix Agents to the Server
1. Add a New Host
<img width="1270" height="654" alt="Add a New Host (Linux(" src="https://github.com/user-attachments/assets/55242913-46fc-437c-86b8-382d45ac51ac" />

2. Check if the Agents are Connected Correctly
<img width="1675" height="132" alt="Agents Connected Correctly8" src="https://github.com/user-attachments/assets/8cb82b3c-329e-44db-beeb-aaf9ad455ef2" />




