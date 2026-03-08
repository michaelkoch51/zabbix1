
# zabbix1
## Использованные команды

### Установка и настройка агента на VM1 (Zabbix Server)
sudo apt install zabbix-agent

sudo nano /etc/zabbix/zabbix_agentd.conf
# В файле: Server=127.0.0.1, ServerActive=127.0.0.1, Hostname=Zabbix-Server-VM1

sudo systemctl restart zabbix-agent
sudo systemctl enable zabbix-agent
ВМ2
wget https://repo.zabbix.com/zabbix/7.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_7.0-2+ubuntu24.04_all.deb
sudo dpkg -i zabbix-release_7.0-2+ubuntu24.04_all.deb
sudo apt update
sudo apt install zabbix-agent

sudo nano /etc/zabbix/zabbix_agentd.conf# В файле: Server=<IP_Zabbix_Server>, ServerActive=<IP_Zabbix_Server>, Hostname=Ubuntu-VM2

sudo systemctl restart zabbix-agent
sudo systemctl enable zabbix-agent
ПРоверка логов
sudo tail -f /
---

