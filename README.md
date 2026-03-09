# Задание 1  
Команды
wget https://repo.zabbix.com/zabbix/7.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_7.0-2+ubuntu24.04_all.deb  
sudo dpkg -i zabbix-release_7.0-2+ubuntu24.04_all.deb  
sudo apt update  
apt install zabbix-server-pgsql zabbix-frontend-php php8.3-pgsql zabbix-apache-conf zabbix-sql-scripts zabbix-agent  
sudo -u postgres createuser --pwprompt zabbix  
sudo -u postgres createdb -O zabbix zabbix  
проверяем статус и логи  
sudo tail -f /var/log/zabbix/zabbix_agentd.log  
sudo systemctl status zabbix-agent  
zabbix_agentd -t system.cpu.load  
sudo tail -f /var/log/zabbix/zabbix_agentd.log  
 /etc/zabbix/zabbix_server.conf - отредактировал  
systemctl restart zabbix-server zabbix-agent apache2  
systemctl enable zabbix-server zabbix-agent apache2  

Первая машина у меня ubuntu 24.04, вторая Kali linux, все делал через Макбук М1 виртуалбокс

# Задание 2  

Команды:  

агент был установлен ранее на локалхост, на вторую машину Kali linux:  

wget https://repo.zabbix.com/zabbix/7.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_7.0-2+ubuntu24.04_all.deb  
sudo dpkg -i zabbix-release_7.0-2+ubuntu24.04_all.deb   

apt update  
 
apt install zabbix-agent  

systemctl restart zabbix-agent  

systemctl enable zabbix-agent  
 
  
<img width="614" height="382" alt="Снимок экрана 2026-03-09 в 10 10 27" src="https://github.com/user-attachments/assets/4179bb67-7a28-439b-bb10-430131489840" />  


<img width="775" height="411" alt="Снимок экрана 2026-03-09 в 10 57 08" src="https://github.com/user-attachments/assets/8f70f2d2-504a-4a93-9e6c-9b34aa12c5e5" />  


<img width="625" height="387" alt="Снимок экрана 2026-03-09 в 19 06 25" src="https://github.com/user-attachments/assets/ea1e21ec-c4a6-4a03-8c92-9d4de8ee4852" />  

<img width="619" height="380" alt="Снимок экрана 2026-03-09 в 19 05 37" src="https://github.com/user-attachments/assets/aefc3205-0ec0-4e75-9c94-448593d82411" />  

<img width="437" height="352" alt="Снимок экрана 2026-03-08 в 15 54 51" src="https://github.com/user-attachments/assets/f0e861df-9cdd-47ec-98dd-54ad47bff8bd" />  


