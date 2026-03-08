Команды добавил
# zabbix1
Установка и настройка агента на VM1 (Zabbix Server)
sudo apt install zabbix-agent
sudo nano /etc/zabbix/zabbix_agentd.conf
# В файле: Server=127.0.0.1, ServerActive=127.0.0.1, Hostname=Zabbix Server
sudo systemctl restart zabbix-agent
sudo systemctl enable zabbix-agent

ВМ2 zabbix_server1

wget https://repo.zabbix.com/zabbix/7.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_7.0-2+ubuntu24.04_all.deb
sudo dpkg -i zabbix-release_7.0-2+ubuntu24.04_all.deb
sudo apt update
sudo apt install zabbix-agent
sudo nano /etc/systemd/system/zabbix-agent.service
sudo systemctl daemon-reload
sudo systemctl stop zabbix-agent
sudo systemctl start zabbix-agent
sudo systemctl enable zabbix-agent
sudo tail -f /var/log/zabbix/zabbix_agentd.log
sudo systemctl status zabbix-agent
zabbix_agentd -t system.cpu.load
sudo tail -f /var/log/zabbix/zabbix_agentd.log
<img width="437" height="352" alt="Снимок экрана 2026-03-08 в 15 54 51" src="https://github.com/user-attachments/assets/f0e861df-9cdd-47ec-98dd-54ad47bff8bd" />
<img width="637" height="385" alt="Снимок экрана 2026-03-08 в 16 01 24" src="https://github.com/user-attachments/assets/a240d744-4657-4c2b-ab68-250c01cab753" />
<img width="636" height="382" alt="Снимок экрана 2026-03-08 в 16 05 30" src="https://github.com/user-attachments/assets/3455fcac-d8ba-48b0-a5c1-76642533ed2c" />
<img width="432" height="327" alt="Снимок экрана 2026-03-08 в 16 11 32" src="https://github.com/user-attachments/assets/0b1a24a2-3473-4de7-bcb9-cc7c1cc0feb6" />
