Задание 1  
Установите Prometheus.  
    
Процесс выполнения  
Выполняя задание, сверяйтесь с процессом, отражённым в записи лекции  
Создайте пользователя prometheus  
Скачайте prometheus и в соответствии с лекцией разместите файлы в целевые директории  
Создайте сервис как показано на уроке  
Проверьте что prometheus запускается, останавливается, перезапускается и отображает статус с помощью systemctl  
Требования к результату  
Прикрепите к файлу README.md скриншот systemctl status prometheus, где будет написано: prometheus.service — Prometheus Service Netology Lesson 9.4 — [Ваши ФИО]  
 
![image](https://github.com/user-attachments/assets/108d06d0-6a9a-4ef4-9a01-fba758733b5e)


Задание 2
Установите Node Exporter.

Процесс выполнения
Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
Скачайте node exporter приведённый в презентации и в соответствии с лекцией разместите файлы в целевые директории
Создайте сервис для как показано на уроке
Проверьте что node exporter запускается, останавливается, перезапускается и отображает статус с помощью systemctl
Требования к результату
Прикрепите к файлу README.md скриншот systemctl status node-exporter, где будет написано: node-exporter.service — Node Exporter Netology Lesson 9.4 — [Ваши ФИО]

![image](https://github.com/user-attachments/assets/6e66a87e-2fb6-45b9-b0e8-f926512b4a08)

Задание 3
Подключите Node Exporter к серверу Prometheus.

Процесс выполнения
Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
Отредактируйте prometheus.yaml, добавив в массив таргетов установленный в задании 2 node exporter
Перезапустите prometheus
Проверьте что он запустился
Требования к результату
 Прикрепите к файлу README.md скриншот конфигурации из интерфейса Prometheus вкладки Status > Configuration
 Прикрепите к файлу README.md скриншот из интерфейса Prometheus вкладки Status > Targets, чтобы было видно минимум два эндпоинта

![image](https://github.com/user-attachments/assets/e22028da-9d61-4f32-866d-66de735761f3)

![image](https://github.com/user-attachments/assets/d7c09a64-4af7-4f56-bce3-54292361ad5f)


Задание 4*
Установите Grafana.

Требования к результату
 Прикрепите к файлу README.md скриншот левого нижнего угла интерфейса, чтобы при наведении на иконку пользователя были видны ваши ФИО


![image](https://github.com/user-attachments/assets/b7c05608-e38f-480a-8992-e0606047ec5c)

Задание 5*
Интегрируйте Grafana и Prometheus.

![image](https://github.com/user-attachments/assets/562e8f34-4320-47f9-a53e-4158376c38f4)





 
