Задание 1
Установите Zabbix Server с веб-интерфейсом.

Процесс выполнения
Выполняя ДЗ, сверяйтесь с процессом отражённым в записи лекции.
Установите PostgreSQL. Для установки достаточна та версия, что есть в системном репозитороии Debian 11.
Пользуясь конфигуратором команд с официального сайта, составьте набор команд для установки последней версии Zabbix с поддержкой PostgreSQL и Apache.
Выполните все необходимые команды для установки Zabbix Server и Zabbix Web Server.
Требования к результатам
Прикрепите в файл README.md скриншот авторизации в админке.
Приложите в файл README.md текст использованных команд в GitHub.

Использованные команды:

1.mkdir zabbix && cd zabbix &&  wget https://repo.zabbix.com/zabbix/7.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_latest_7.0+ubuntu22.04_all.deb

2.dpkg -i zabbix-release_latest_7.0+ubuntu22.04_all.deb

3.apt install zabbix-server-pgsql zabbix-frontend-php php8.1-pgsql zabbix-apache-conf zabbix-sql-scripts zabbix-agent

4.sudo apt install postgresql

5.sudo -u postgres psql --command "create user zabbix with password '12345';"

6.sudo -u postgres psql --command "CREATE DATABASE zabbix OWNER zabbix;

7.zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix

![image](https://github.com/user-attachments/assets/e2fe4ddb-cfbb-4383-8990-0a9445c7c62b)



### Задание 2

Установите Zabbix Agent на два хоста.

Процесс выполнения
Выполняя ДЗ, сверяйтесь с процессом отражённым в записи лекции.
Установите Zabbix Agent на 2 вирт.машины, одной из них может быть ваш Zabbix Server.
Добавьте Zabbix Server в список разрешенных серверов ваших Zabbix Agentов.
Добавьте Zabbix Agentов в раздел Configuration > Hosts вашего Zabbix Servera.
Проверьте, что в разделе Latest Data начали появляться данные с добавленных агентов.
Требования к результатам
Приложите в файл README.md скриншот раздела Configuration > Hosts, где видно, что агенты подключены к серверу
Приложите в файл README.md скриншот лога zabbix agent, где видно, что он работает с сервером
Приложите в файл README.md скриншот раздела Monitoring > Latest data для обоих хостов, где видны поступающие от агентов данные.
Приложите в файл README.md текст использованных команд в GitHub

![image](https://github.com/user-attachments/assets/2a2d75ab-42c0-468b-a9d2-81c5350b78f1)


![image](https://github.com/user-attachments/assets/3ad8907e-d326-4780-b9c2-a3e8ec45b76b)


![image](https://github.com/user-attachments/assets/e6b9361c-afd7-4b6d-be47-d4d7779e4fb2)



Использованные команды:

1.sudo apt install zabbix-agent

2.tail -f /var/log/zabbix/zabbix_agentd.log

3.systemctl restart zabbix-agent

